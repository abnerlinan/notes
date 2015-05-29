#Command Line API

The Firebug Command Line provides these special functions for your convenience. These include functions to control the Firebug UI, functions interacting with the page, shortcuts for selectors and shortcuts for the Console API. Other browsers implement the Command Line API as well; the Chrome DevTools, Safari Inspector and Opera Dragonfly, implement most of what is below.

###help

Returns a list of Command Line API commands including short descriptions.

###$(selector)

Returns a single element matching the given CSS selector.

In old Firebug versions, this used to be equivalent to document.getElementById.

###$$(selector)

Returns an array of elements that match the given CSS selector.

###$x(xpath[, contextNode[, resultType] ])

Returns an array of elements that match the given XPath expression.

###$0

Represents the last element selected via the Inspector.

###$1

Represents the second last element selected via the Inspector.

###$_

Returns the value of the most recently evaluated expression in the Command Line.

###$p

A container of arbitrary JavaScript values, after right-clicking them and selecting "Use in Command Line".

###$n(index)

Returns one of the 5 last elements selected via the Inspector. This method takes one required parameter index, which represents the index of the element (starting at 0).

###dir(object)

Prints an interactive listing of all properties of the object. This looks identical to the view that inside the DOM Panel.

###dirxml(node)

Prints the XML source tree of an HTML or XML element. This looks identical to the view inside the HTML Panel. You can click on any node to inspect it in the HTML panel.

###cd(window)

By default, command line expressions are relative to the top-level window of the page. cd() allows you to use the window of a frame in the page instead.

###clear()

Clears the console.

###copy(object)

Copies the given parameter to the clipboard. This can be a return value of a function or an object.

###inspect(object[, panelName])

Inspects an object in the most suitable panel, or the panel identified by the optional argument panelName.

The available tab names are "html", "stylesheet", "script", and "dom".

###keys(object)

Returns an array containing the names of all properties of the object.

###values(object)

Returns an array containing the values of all properties of the object.

###include(url[, alias]) / include(alias)

Includes a remote script.

###debug(fn)

Adds a breakpoint on the first line of a function.

###undebug(fn)

Removes the breakpoint on the first line of a function.

###monitor(fn)

Turns on logging for all calls to a function.

###unmonitor(fn)

Turns off logging for all calls to a function.

###monitorEvents(object[, types])

Turns on logging for all events dispatched to an object. The optional argument types may define specific events or event types to log.

###unmonitorEvents(object[, types])

Turns off logging for all events dispatched to an object. The optional argument types may define specific events or event families, for which to turn logging off.

For a list of available event families see monitorEvents(object[, types]).

###profile([title])

Turns on the JavaScript profiler. The optional argument title contains the text to be printed in the header of the profile report.

###profileEnd()

Turns off the JavaScript profiler and prints its report.

###table(data[, columns])

This is a shortcut for console.table().

###traceCalls(fn)

Enables tracing of specific function calls.

###untraceCalls(fn)

Disables tracing of specific function calls.

###traceAll()

Enables tracing of function calls for a whole context.

###untraceAll()

Disables tracing of function calls for a whole context.

###getEventListeners()

Returns all the event listeners registered for specific node (event target).
