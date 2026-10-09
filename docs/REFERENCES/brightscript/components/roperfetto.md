---
title: roPerfetto
excerpt: 'Add custom events and heap graph captures to a Perfetto trace of your app'
deprecated: false
hidden: false
metadata:
  title: 'roPerfetto'
  description: 'The roPerfetto component lets you add instant, duration, scoped, and flow events to a Perfetto trace of your app, and capture heap graphs from BrightScript.'
  robots: index
next:
  description: ''
---
The **roPerfetto** component lets you add your own events to the [Perfetto](https://perfetto.dev/docs/) trace of your app. You can mark instantaneous events (such as a key press), events with a duration (such as a long function), scoped events, and flows of events that cross threads. You can also capture a heap graph of your app's BrightScript and SceneGraph objects.

Events you add with roPerfetto appear in the trace alongside the events that Roku OS records. You can then view and query them in the [Perfetto UI](https://ui.perfetto.dev).

> roPerfetto events are recorded only when tracing is enabled for the app and a trace is being captured. For the requirements and the steps to enable and record a trace, see [Roku app tracing (with Perfetto)](doc:app-tracing).
>
> Perfetto tracing is available only for apps that run as a process. For a sideloaded app, set `run_as_process=1` in the manifest.

**Example: Adding a custom event to a trace**

```brightscript
sub init()
    tracer = CreateObject("roPerfetto")
    tracer.instantEvent("app_started", {build: "1.4.2"})
end sub
```

## Supported interfaces

* [ifPerfetto](doc:ifperfetto)
