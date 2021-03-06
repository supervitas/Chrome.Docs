This page is deprecated. It's contents have been moved to [Mozilla Developer Network](https://developer.mozilla.org/en-US/)

# Window.requestIdleCallback()

The **`Window.requestIdleCallback()`** method enables the scheduling of tasks during a browser's idle periods. This enables developers to perform background and low priority work on the main event loop, without impacting latency-critical events such as animation and input response.

## Syntax

`var handle = Window.requestIdleCallback(callback[, options])`

### Returns

An unsigned long integer that can be used to cancel the callback using the [cancelIdleCallback()](Window.cancelIdleCallback.md) method.

### Parameters

<dl>
  <dt><code>callback</code></dt>
  <dd>A reference to a function that will be called during a browser's idle period. The callback function must take the following parameters:
    <ul>
      <li><code>timeRemaining</code>: A reference to a method that returns a {{domxref("DOMHighResTimeStamp")}}.</li>
      <li><code>didTimeout</code>: A boolean that returns true if the callback was invoked by the user agent, and false otherwise.</li>
    </ul>
  </dd>
  <dt><code>options</code> {{optional_inline}}</dt>
  <dd>Contains optional configuration parameters. It has the following property:
    <ul>
      <li><code>timeout</code>: A deadline by which the browser must call the given callback function. This value is given in milliseconds.</li>
    </ul>
  </dd>
</dl>


## Specifications

<https://w3c.github.io/requestidlecallback/>
