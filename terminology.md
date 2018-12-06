# REST Model

REST is a style for designing distributed systems.

The subjects of interest in these distributed systems are [resources](#resource).

#### Resource
A resource is a stateful, named entity.

The state of a resource may change over time. A resource is governed by an entity that is authoritative for the resource state and is named by a resource identifier.

#### Interaction
An interaction in these distributed systems is the remote invocation of a method on a resource in [client](#client)-[server](#server)/[request](#request)-[response](#response) style, transferring [representations](#representation) of various kinds.

#### Client
A client is an entity that has the initiative to invoke a method on a [resource](#resource) by making a [request](#request) to a [server](#server).

#### Server
A server is an entity that applies a [requested](#request) method to a [resource](#resource) and conveys the outcome back to the [client](#client) by returning a [response](#response).

#### Request
A request specifies the [resource](#resource) targeted by the method invocation and the method to invoke. Depending on the method, a request may contain a [representation](#representation) and further request parameters.

#### Response
A response specifies the outcome of invoking a method on a [resource](#resource). Depending on the outcome, a response may contain a [representation](#representation) and further response parameters.

#### Representation
A representation is the serialization, for example, of a (current or desired) resource state or an outcome, as a sequence of bytes, labeled with metadata.

#### Augmented Representation
An augmented representation refers to not only a single document of a specific media type, but also any metadata serialized through other protocol capabilities, and additional linked documents that contain further metadata that facilitates constructing affordances from the initial representation document.

A processing model may define a transformation from the representation, other message parameters, retrieval context and externally referenced information that leads to the augmented representation.

#### Representation Format
A defined structure for a [representation](#representation).
Often specified by a Content-Type, which can employ a Media-Type name plus parameters.

#### Stateless
Every [request](#request) is expected to not assume any state at a server other than resource state. (In particular, any state from a previous interaction that was not the result of applying the method to the resource.)

#### Uniform Interface
Every [resource](#resource) is expected to offer (a subset of) the same, small, standardized set of methods.

#### Agent
An agent in these distributed systems is an entity that has the authority to decide which, if any, [interaction](#interaction) is appropriate and to carry out this interaction on behalf of a stakeholder.

#### User Agent
A user agent is an [agent](#agent) that is acting on behalf of a user.



# Hypermedia Model

#### Hypermedia Agent
A hypermedia agent is an [agent](#agent) that makes use of [hypermedia controls](#hypermedia-control) to inform its decisions.

#### Hypermedia Control
A hypermedia control is an [affordance](#affordance) serialized as a part of a [representation](#representation) and/or request/response parameter.
A [representation](#representation) may also be augmented with hypermedia controls through indirection.

#### Hypermedia Control
A hypermedia control is an affordance expressed by or through a message which may be embedded, externally resolved through metadata or indirection, or included within a metadata container of a mediaType.

> Issue: "embedded" vs "included within a metadata container of a mediaType" -- what is the difference?

> answer: protocol = embedded vs mediaType = included


#### Link
A link is a [hypermedia control](#hypermedia-control) that affords an [agent](#agent) to [navigate](#navigation) from one [resource](#resource) to another.
A link describes a directed, typed connection between two [resources](#resource). Depending on the link, it may contain further metadata.

#### Context
Do not use, too many meanings.  Always use the full term, such as:
    
#### Link Context

#### Retrieval Context

#### Navigation

#### Affordance



# The Web

The Web is a distributed system in REST style.

#### Web Resource
A Web resource is a a [resource](#resource) that can be interacted with through a [Web transfer protocol](#web-transfer-protocol).

#### Web Server
A Web server is the authority for a [Web resource](#web-resource).

#### Web Transfer Protocol
A Web transfer protocol is a network protocol such as HTTP and CoAP that facilitates the transfer of request and response [messages](#message).

#### Message

> Header and payload(?).

#### Content

> A representation(?). May be spread across multiple payloads. Labeled with a [content type](#content-type) and [content coding](#content-coding) or a [content format](#content-format).

#### Media Type
A media type is a string of characters such as "text/plain" that identifies a (potentially parameterizable) [representation format](#representation-format).

#### Content Type
A content type is a string of characters such as "text/plain; charset=utf-8" that identifies and parameterizes a [representation format](#representation-format).

#### Content Coding  
A content coding is an encoding transformation applied to a [representation](#representation), such as Gzip compression.

#### Content Format
The combination of a [content type](#content-type) and a [content coding](#content-coding).

#### Web Origin  
A Web origin is a scheme/host/port triple \[[RFC 6454](https://tools.ietf.org/html/rfc6454)\].

#### URI
A URI (Uniform Resource Identifier) is a string of characters that identifies a [Web resource](#web-resource) in a standardized, uniform way \[[RFC 3986](https://tools.ietf.org/html/rfc3986)\].

#### URI Reference
A URI reference is either a [URI](#uri) or a relative reference. A relative reference can be resolved to a [URI](#uri) through the process of reference resolution using a base URI.
