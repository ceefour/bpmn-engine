Activity
========

Base of all bpmn activity types.

<!-- toc -->

- [API](#api)
  - [`execute([message])`](#executemessage)
  - [`signal([output])`](#signaloutput)
  - [`cancel()`](#cancel)
  - [`getState()`](#getstate)
  - [`resume(activityState)`](#resumeactivitystate)
  - [`discard([discardedFlow[,rootFlow]])`](#discarddiscardedflowrootflow)
- [Events](#events)
  - [`enter`](#enter)
  - [`leave`](#leave)

<!-- tocstop -->

# API

## `execute([message])`
## `signal([output])`
## `cancel()`

Cancels execution and takes all outbound sequence flows.

## `getState()`

Get activity state.

- `id`: Activity id
- `type`: Activity type
- `entered`: The activity is entered, i.e. in a running state

## `resume(activityState)`

Resume execution. Resumed with data from [`getState()`](#getstate).

## `discard([discardedFlow[,rootFlow]])`

Cancels execution and discards all outbound sequence flows.

- `discardedFlow`: Optional. Sequence flow instance that was discarded
- `rootFlow`: Optional. First sequence flow instance that was discarded

# Events

## `enter`
## `leave`