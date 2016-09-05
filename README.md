![Logo](Art/Logo150x150.png "Logo")

# Genesis.Observables

[![Build status](https://ci.appveyor.com/api/projects/status/8wjfp853462kea3e?svg=true)](https://ci.appveyor.com/project/kentcb/genesis-observables)

## What?

> All Genesis.* projects are formalizations of small pieces of functionality I find myself copying from project to project. Some are small to the point of triviality, but are time-savers nonetheless. They have a particular focus on performance with respect to mobile development, but are certainly applicable outside this domain.
 
**Genesis.Observables** is a simple library that provides commonly used, pre-canned observables. It is delivered as a PCL targeting a wide range of platforms, including:

* .NET 4.5
* Windows 8
* Windows Store
* Windows Phone 8
* Xamarin iOS
* Xamarin Android

## Why?

When writing reactive code, you will frequently needs empty, default, or other observables. Whilst you can easily create these via methods such as `Observable.Empty<T>()`, doing so will create a new object every time. Since these observables are cold, it makes sense to share a single instance. Doing so can reduce memory pressure. This is particularly useful in mobile applications, or other environments where memory is far more constrained than it is in desktop environments.

## Where?

The easiest way to get **Genesis.Observables** is via [NuGet](http://www.nuget.org/packages/Genesis.Observables/):

```PowerShell
Install-Package Genesis.Observables
```

## How?

**Genesis.Observables** is super simple to use. It provides only two static classes, both obvious in their usage.

Here are some examples:

```C#
// use the Observable<T> class to get commonly-required observables of any type
var emptyI = Observable<int>.Empty;
var neverF = Observable<float>.Never;
var defaultS = Observable<string>.Default;

// use the Observables class to get other commonly required observables
var t = Observables.True;
var f = Observables.False;  // this is the same as Observable<false>.Default, but provided for convenience
var u = Observables.Unit;   // this is the same as Observable<Unit>.Default, but provided for convenience
```

## Who?

**Genesis.Observables** is created and maintained by [Kent Boogaart](http://kent-boogaart.com). Issues and pull requests are welcome.