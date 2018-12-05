# REST Model

REST is a style for designing distributed systems.

The subjects of interest in these distributed systems are resources.

*[Resource]*  
A resource is a stateful, named entity.

The state of a resource may change over time. A resource is governed by an entity that is authoritative for the resource state and is named by a resource identifier.

*[Interaction]*  
An interaction in these distributed systems is the remote invocation of a method on a resource in client-server/request-response style, transferring representations of various kinds.

*[Client]*  
A client is an entity that has the initiative to invoke a method on a resource by making a request to a server.

*[Server]*  
A server is an entity that applies a requested method to a resource and conveys the outcome back to the client by returning a response.

*[Request]*  
A request specifies the target resource of the method invocation and the method to invoke. Depending on the method, a request may contain a representation and further request parameters.

*[Response]*  
A response specifies the outcome of invoking the method on the resource. Depending on the outcome, a response may contain a representation and further response parameters.

*[Representation]*  
A representation is the serialization, for example, of a (current or desired) resource state or an outcome, as a sequence of octets^Wbytes, labeled with metadata.

*[Augmented Representation]*  
An augmented representation refers to not only a single document of a specific media type, but also any metadata serialized through other protocol capabilities, and additional linked documents that contain further metadata that facilitates constructing affordances from the initial representation document.

A processing model may define a transformation from the representation, other message parameters, retrieval context and externally referenced information that leads to the augmented representation.

*[Representation Format]*  
A defined structure for a representation.
Often specified by a Content-Type, which can employ a Media-Type name plus parameters.

*[Stateless]*  
Every request is expected to not assume any state at a server other than resource state. (In particular, any state from a previous interaction that was not the result of applying the method to the resource.)

*[Uniform Interface]*  
Every resource is expected to offer (a subset of) the same, small, standardized set of request methods.

*[Agent]*  
An agent in these distributed systems is an entity that has the authority to decide which, if any, interaction is appropriate and to carry out interactions on behalf of a stakeholder.

*[User Agent]*  
A user agent is an agent that is acting on behalf of a user.



# Hypermedia Model

*[Hypermedia Agent]*  
A hypermedia agent is an agent that makes use of hypermedia controls to inform its decisions.

*[Hypermedia Control]*  
A hypermedia control is an affordance serialized as a part of a representation and/or request/response parameter.
A representation may also be augmented with hypermedia controls through indirection.

*[Hypermedia Control]*  
A hypermedia control is an affordance expressed by or through a message which may be embedded, externally resolved through metadata or indirection, or included within a metadata container of a mediaType.

> Issue: "embedded" vs "included within a metadata container of a mediaType" -- what is the difference?

> answer: protocol = embedded vs mediaType = included


*[Link]*  
A link is a hypermedia control that affords an agent to navigate from one resource to another resource.
A link describes a directed, typed connection between two resources. Depending on the link, it may contain further metadata.

*[Context]*  
Do not use, too many meanings.  Always use the full term, such as:
    
*[Link Context]*  

*[Retrieval Context]*  

*[Navigation]*  

*[Affordance]*  



# Related Terms

*[Media Type]*  
A sequence of characters such as "text/plain" that identifies a (potentially parameterizable) representation format.

*[Content Type]*  
A sequence of characters such as "text/plain; charset=utf-8" that identifies and parameterizes a representation format.

*[Content Format]*  
The combination of a content type and a content coding.

*[Origin]*  
Scheme + Authority ([RFC 6454](https://tools.ietf.org/html/rfc6454)).  A term not relevant to and preferably avoided in the present discussion.
