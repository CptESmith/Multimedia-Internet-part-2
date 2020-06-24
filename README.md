
# Multimedia Internet  part 2

## Mobile telephony quality 90s VS mobile telephone quality now
Mobile telephony quality in the 90s was equal and, in some cases, better than the quality we have now. There are various reason for that:

 - **Handset design:** phone today's main focus is not voice quality, so the speaker and the microphone can be misplaced, for example they can be very near. *Solution:*  using multiple microphones.
 - **Sharp background noise:** background noise is filtered, but when it comes to sudden sounds can be difficult to eliminate them. *Solution:* using specialized headsets with noise cancelling technology.
 - **Phone to tower connection:** the distance from a cellular tower can degrade the quality of a voice call. *Solution:* signal booster for telephones.
 - **Voice data conversion:** cellular voice phone calls can be compressed and unpacked various times, degrading the voice quality. *Solution:* VoLTE can compress the voice signal only once.
 > **VoLTE:** it is a solution on the network side, where we give voice packets a better treatment respect to other type of packets to limit their delay.
 
## IP interconnection

The internet is a collection of networks called Autonomous Systems, that are administered by independent entities. The interconnection between two AS is a private contract between the two administrators. Usually traffic across interconnection interfaces is treated as best effort.
- **Transit:** between a larger AS and a smaller one, and it is payed for.
- **Peering:** the ASs have similar size, not transitive. Is the preferred choice when possible because they don't have to pay each other or pay very little respect to transit.
Various players:
- **Tier 1 operator:** can reach every IP address in the world without buying transit services, but just with its network or peering contracts.
- **Over The Top Providers (OTTP):** e.g. Google, they are service provider without a network.
- **Content Provider:** e.g. Netflix, they are a problem for Telcos because there's gonna be more content with pay per view requested by users without generating more money for the Telco, but only adding expense to them.
- **Service Provider:**
- **Content Delivery Network (CDN):** 
> A **cache** is a server that can store a content while it is transiting. They are placed in strategical points where the traffic is more intense. If a content is highly requested is convenient to store it in the cache. Caches can be place at high or low hierarchical level. Some advantages are: performance and quality, and reducing the transit diminishing costs. They have inside them the **Content Database**.

## Net neutrality
The approach is not to differentiate service on user identity, but to differentiate it based on which type of application the packets are from. E.g. VOIP buffer has priority over data buffer.
Business in the internet is regulated by rules and laws that have technical consequences. The debate has been centered around policy, law and finance as if the network was a given thing, but it is not.

## Next Generation Network (NGN)
In the traditional access network all the links are made of copper apart the link between the Central Office (CO) and the Service Distribution Frame (SDF), which is fiber. The copper links have a series of disadvantages respect to the fiber:
- collect more external noise
- create more natural interferences
- degradation due to humidity
- narrower (smaller) bandwidth

NGN is not simply a substitution of copper with fiber, also the architecture of the access network changes.

 - **FTTE**, Fiber To The Exhchange: very simple cabinets who don't need power because they are all mechanical electrical (no electronics). They are cheap, they need low manteinance and are unnoticed by people. Not very interesting.
 - **FTTC**, Fiber ToThe Cabinet: they have lot of problems because the technology is mixed (optical and electronics), and it requires advanced tech that consumes power and occupies a large space (vandalism is possible). The street cabinet needs electrical power, and they also need air conditioning.
 - **FTTB**, Fiber ToThe Building: the Service Distribution Frames (SDF) are all optical (passive) and underground (small). There are some issues similar to the FTTC street cabinet, but they are inside the building so vandalism is less of a problem and they have an easy life in accessing power.
 - **FTTH**, Fiber To The Home: All the connections from the Central Office (CO) to the house are passive. It is possible to have the same speed in uplink and in downlink. The main problem is that the deployment is complicated because it is difficult to pass the fiber form the sidewalk to the basement of the building.
 > There are two types of FTTH:
 > - **P2P**, Point To Point: there is a dedicated fiber to each user.
 > - **PON**, Passive Optical Network: a tree structured network of fibers where the capacity of the fiber is shared among users. Only passive devices are used. The main advantage is the cost, while the disadvantages are the performance (bandwidth shared among users), and the privacy.
 > *TDM-PON*, Time Division Multiplexing: it separates uplink and downlink through wave division. *Shared PON:*  easier to assign users to operators, and also sharing an infrastructure diminishes costs for the operators.
 # Unbundling and colocation
 Operations of changing an operator; they are mandatory and cannot be refused.
 The cost of this operation varies depending on where you change operator:
 - **Unbundling:** the closest to the final user, the cheapest. The closest to the CO, the highest price.
 - **Colocation:** substituting one operator in the Optical Line Terminal (OLT) that is inside the CO.
 > **OLO,** Other Licensed Operators: new operators that are not former state company (**incumbent operators**).

# Business issues for operators
The deployment of the NGAN must be balanced between costs for the operatore and average money that the user will pay. The costs are not uniform, and they depend on the kind of territory:
- **Metropolitan** areas: the deployment cost per user is low since the population density is high, and the costs are likely to be repayed by the costumers.
- **Suburban** areas: middle costs and middle payment from the costumers between the two other cases.
- **Rural/mountain** areas: from a business POV they are not convenient, because the population is sparse and the difficulties for deploying the fiber are high. In this case the state get involved contributing to the investment to permit even the people that live in less dense places to have NGAN.
# Services of operators
In a Next Generation Access Network (NGAN) the services provided are:
- **intermediate service:** a typical example is the connection of mobile network antennas to the core network aka *backhauling*. Another example is the tube rental, where an operator rents tube to other operators.
> Various solutions for backhauling:
> - E1 lines for backhauling, not the best way because we have to mantain two different systems.
> - GPS: the signal is stable enough, but it is not the best idea because the GPS system is property of the USA, and they can decide to turn it off at any moment.
> - Pseudowire: the PW packets will be characterized by a guaranteed SLA, while other packets will have a statistical SLA.
- **wholesale service:** inter-operator services like wholesale line rental, wholesale leased line, unbundling, colocation. Wholesale services are not traded in single units, but in large stocks.
- **retail service**

The basi requirements for operators to trade this kind of services are that the QoS must be negotiable both at the connection setup and when the connection is established, and there is also have to be a minimal list of voice, audio and video coders that should be supported.

# Telephony Over IP (TOIP)
IP telephony is a replacements for Plain Old Telephone Service (POTS). It has to have some services possible:
- numbering plan must be preserved
- lawful interception must be guaranteed
- malicious call identification must be possible
- anonymous call rejection must be possible
- interoperability with POTS guaranteed

Is TOIP a full replacement of POTS? Not really.

# Multimedia streaming
It is the distribution of audio and video content. The content is consumed during its transfer. 
>Two main flavors:
>- **PUSH:** provider distributes contents based on a time schedule
>- **PULL:** users can ask for any content any time, it has higher costs and it is more difficult caching and multicasting.

The chain of the service stream is composed by:
- DB, where is stored the content
- server
- coder, to make the content format compatible with network transportation
- network
- playout buffer
- playout service

The media transfer is unidirectional form the server to the client.
The control informations (*signaling*) on the control plane are bidirectional, and they are used to set up the connection, to negotiate the media, to get quality feedback in real time, to interact with the playout and to tear down the connection.
- Streaming **unicast:** one distribution flow per user; total bandwidth required.
- **Caching:** caches store contents and they replay stored content for new users requiring them; smaller bandwidth require. It can be done at different levels: higher is closer to the interconnection, lower is closer to the user.
- **Proxy server:** owned and managed by the Service Provider (SP).
- Streaming **multicast:** ideal way of streaming the media, using multicast distribution. It is hard to use because most network do not support multicasting (IP for example, it has a primitive multicasting capacity adn cannot support high bandwidth services).


# Internet protocols
Internet protocols are the structure and the format of messages. They are normally client-server protocols, where a client sends a request to a server, and the server replies with a response. The ones we are interested in are:
- HTTP (HyperText Transfer Protocol): plaintext, not encrypted
- HTTPS: information is encrypted
- SIP, RTSP: specific for signaling

A typical HTTP request message has the following structure:

>request line \r\n
header line 1\r\n
header line 2\r\n
...
header line n\r\n
\r\n
body\r\n

The first line and the header lines are text strings, and they are separated by the *line separator* \r\n. The additional line separator after the last header line marks the start of the body of the message. There is no line terminator after the last byte of the body, so the **content length** is fundamental because it identifies univocally the last byte of the current message.

The **request line** (first line of the message) has the following structure:
> method request-uri protocol-version

It has three fields separated by a single space character. The first one is the method, that specifies the kind of action that the requesting entity would like to perform. The second field specifies which is the resource on which the action must be performed, and the third field which specifies the protocol identity and version.
Example:
> GET /serviceA?parameter=n_request HTTP/1.1

The second parameter is partial, the complete one can be for example:
> http://myservice.com/serviceA?parameters.required=n_requests

If the **Universal Resource Identifier (URI)** starts with http:// it means that we are using the HTTP protocol.
The name of the headers are standardized. The headers are divided into four categories:
- **general headers:** provide details on the connection between the server and the client. It can be connection: close or connection: keep alive.
> there are two main way to establish and maintain a connection. In the first case for every request a connection is established and closed. In the second case we maintain a connection for multiple requests, a more efficient way to use a connection with latency diminishing and throughput improving. In the second case we can also use **pipeline:** the client sends requests even if it has not received the responses of the previous messages. In this way we can improve a lot the throughput.
- **request headers:,** there are various methods: GET, PUT POST, POST (to make a complicated request), DELETE.
- **response headers,** same structure of a request message, but it can use some headers that are not used by request messages, for example HTTP/1.1 200 OK.
- **entity headers:** information about the content carried in the body of the message, for example the content_length header.

The **body** is a sequence of bytes, and it can carry any kind of content: a text, a picture, a video clip, json file... It is *byte clean*, meaning that any value is allowed since there is no interpretation of byte value.

# HTTPS
HyperText Transfer Protocol over Secure Socket Layer
Respect to HTTP adds encryption to the data transfer. In plain HTTP the structure is TCP, HTTP without encryption. In HTTPS the architecture is TCP, TLS (Transport Layer Security), HTTP. TLS can be certificate based (the most common) or Private Shared Key (PSK) based, that is faster, but in which the key is usually not exchanged through the network.

# RTSP
 Real Time Streaming Protocol
 Fully integrated with other important internet protocols such that: HTTP, SDP (Session Description Protocol), RTP (Real Time Protocol). Gives features such: start, pause, jump, fast forward, fast reverse.

# Video server
 System for streaming, started in the 1990s has not a lucky beginning. There are a lot of parameters that should be taken into account:
 - Storage: video files occupies a very large storage space. We need to consider how many contents do we have and how much do they weight. One way to store lot of contents without spending too much money is to use Redundant Array of Inexpensive Disks (RAID). **Replication factor:** how many times we have stored a content, it determines its reliability.
 > There are two main types of hard drives: HDD that are rotational drivers, are slow, but not much expensive and SDD solid state that are much faster, but also more expensive.
 - speed of loading the content
- access time
- cost

The **long tail graph** put in relation the **hit rate** (how many people watches each content) with the number of contents.
We can divide the CPs into two main categories depending of their hit rate:
- **High hit rate:** smaller number of contents, high definition, large storage for each content, payed service, require Ultra Large Bandwidth (ULB) network access, acquisition of content is expensive.
- **Long tail:** large number of contents, low definition, small storage space for each content, free service, doe not require ULB, acquisition of content is mainly free.

# Media formats
A digital video is a sequence of images. The frequency of those images is called **frame rate**. Standard FPS are between 25 and 40, but 8k has more than 100 FPS (UHD). The typical resolution is 1280x720 for HD, 1920x1080 for FULL-HD, that are pixels x pixels. A pixel is a colored dot.
Color spaces:
- **RGB:** it defines the amount of Red, Green and Blue in each pixel
- **YCrCb:** amount of Y luminance (*luma*, the most important), Cr red and Cb blue (the lasts two indicator are called *chroma*). The sampling can be configured 4:4:4 is fully sampled, 4:2:2 has less information, occupies smaller storage and uses less bandwidth and 4:2:0.

The bit rate for transmitting a FULL HD video is too high if the media is not compressed. The formats for storage are different from the formats for transmission. An optimized way to compress video files is compression by prediction that works in most of cases, with some exceptions ( first scene of "Silence of the lamb").

# Video formats
There is no optimal video format for all cases, there is always a trade off between quality and bandwidth. Video files are made of 2 parts:
- **Container:** that is how the file, metadata and data are structured. It contains the metadata and the compressed video data encoded using the codec. Generally is called the *format*, because it reflects the file's extension.
- **Codec:** is the protocol for encoding and decoding the video.

# IPTV and Internet TV
The IPTV (Internet Protocol Television) is a high quality service distribution of digital TV using both dedicated network infrastructure and public internet. The Internet TV is the distribution of the media through the public internet usually with low quality, but smaller bit rate.
IPTV is a linear/push type of content distributor: its programs transmission is scheduled; it can also have an archive with older content, so it can also be a pull type content provider. Internet TV is a non linear/pull type: users ask for a specific content whenever they want.
The users in the IPTV are known and registered and they are authenticated usually with a set of box + smart card, while in the Internet TV the user can be anyone. IPTV is a payed service while Internet TV is free. IPTV has high quality contents while Internet TV have web based content. Contents in IPTV are protected, while contents in Internet TV are not.

# P2P video streaming
We are not gonna study the underlay topology aka the physical layer that can be very long. We focus on the overlay topology that is virtual and build by the nodes autonomously. There are three main overlay topologies: **tree** hierarchical topology, single point of failure, **forest** that is made by multiple trees and resolves the single point of failure problem and **mesh** that is a generic topology, not hierarchical and where a leave event might be unnoticed.
There are also some performance issue with the tree and the forest topology. If the depth of a tree grows too much, the last leafs of are gonna have high delay and packet loss respect to high level nodes. So this type of topologies are particularly effected by the depth of trees, so deep trees should be avoided, but it was not possible to do so until a few years ago (ADSL era, limit on uplink). Wide trees should be preferred.

Construction of topology for tree and forest topologies:
- **join:** when a node wants to join a network.
- **rejoin:** when a node becomes an orphan (the node at which it is connect leave) and it must rejoin the network.

In mesh topology the join and rejoin operations are more complicated, but it can guarantee more performance and stability. Every peer has its own **Buffer Map** (BM) used to keep record of the segments it has received. The peers exchange periodically their BM, and each node builds and maintains in real time the m cache that is a matrix composed by all the BM of the other nodes. When a node needs a segment of a media it knows which peer have it. This type of topology is robust to leave event. The main problem is when a node has too few neighbors. There is an optimal number of neighbors a node should have to not have too many BM exchanges or too less peers to ask for content.

**Node selection:** when a node is joining or rejoining a network, it has to take into account various metrics such as *ping time* .

For tree and forest topologies joining close to the root is better than joining at a leaf, but the competition is stronger. The system might keep track of the stability of a peer, so that the join/rejoin operation close to the root can e done only to high stable peers.

# SIP: Session Initiation Protocol
SIP is a signaling protocol. It handles the set up, tear down and management of IP multimedia sessions. It is naturally integrated with other internet protocols such that SDP, RTSP and SAP (Session Announcement Protocol). SIP usually adopts RTP as a transport for media streams.

SIP is a client/server protocol:
- **Client:** called User Agent Client (UAC), is in the user's device, sends SIP requestes.
- **Server:** there are four types of server proxy, registrar, redirect, User Agent Server (UAS). The last one is in the user's device and receives SIP requests.

**Registrar server:** it handles SIP registration requests. Those requests are used by devices to register into the SIP network and they are mandatory for any device.

**Basic call:** 
- invite message
- PRES (Provisional Response) send back to the caller to signal him that the device of the called user is ringing
- RES: OK, the call has been accepted  and it has been set up
- REQ: BYE, when someone hungs up the call

**Transaction:** a software object that describes the session and in particular its phases.
**Provisional Responses:** are used to let the transaction knows that the request is being processing. PRES are never final, they don't mean that the request has been fully processed. For example in case of long requests the client must know that the request is in processing, so PRES messages are sent periodically from the server to the client to keep the client updated so that he will keep waiting the final response. Sending periodic provisional responses makes the TCP keep the connection alive. This is a problem we don't have with UDP because UDP has no connection.

**SIP messages:** they can be wither requests or responses. SIP has been one of the first signaling protocol to have textual format messages as opposed to traditional signaling protocols in which they are binary. This is usually an advantages even if textual messages consume more bandwidth.
The *request line* specifies the type of request and its parameters.
**Body** of SIP messages: can carry almost everything, it is not standardized like the body of HTTP. The most frequent body is application/SDP that is used for the navigation of the media.

**SIP request methods:** 
- invite, to start a session
-  bye, to close a session
-  register, to register a user in the SIP network
- ack, acknowledge
- options,
- cancel, to cancel a signaling transaction

Request:
> method request URI version\r\n

Response:
> version statuscode reason phrase\r\n

Status code is three digit:
- 1XX: provisional
- 2XX: success, the most important is 200 OK
- 3XX: redirection
- 4XX: bad request failure, the request message is not well formed. E.g. 404 not found: the resource has not been found
- 5XX: server failure
- 6XX: global failure

All messages have **headers:**
- General: (to, from, call ID) is a triplet specific of SIP that identifies called and calling users.
- Request: only used for requests.
- Response: only used for responses.
- Entity: their main purpose is to describe the content of the message body.
- VIA: specifies the SIP route followed by the request message, so that response can use the same path backwards. The response must follow the same path backwards because proxies are generally stateful: they remember the dialogues of the messages that they forward, so via headers are used to guarantee that the SIP path of responses is the backward path of requests.

# Session Description Protocol (SDP)
SDP is used for the description of the format of media streams. For each media stream of a session, an SDP description is needed. SDP descriptions are carried in the body of SIP messages and they enable *media negotiation*.
Media negotiation happens with a two way handshake, and it is very simple compared to the media negotiation of previous signaling protocols like H.323.
> Note that SDP does not trnsport media: it is used only for their description.

# Interworking of signaling
To make different signaling protocols interoperate we use interworking, that is one of the most complex problems of telephony. The two main problems are in the control plane where we use different signaling protocol and in the user plane where we have different media formats.

Media gateways translate the media, while signaling gateways interwork signaling.
Media gateways are controlled by Media Gateway Controllers (MGC) and they communicate using a specialized signaling protocol such as the Media Gateway Control Protocol (MGCP). MGCs and signaling gateway need to intercommunicate, so a gateway architecture is created.

**Soft switch** is a distributed system for interworking that manages separately media and signaling. MH**Soft switch** is a distributed system for interworking. MGCs intercommunicate through SIP. MGCs communicate with media gateways with MGCP.
MGC specifies how a media gateway must translate media, and can require dynamic change ofmedia format.
The basi objects managed by MGCP are theendpoints. MGCP connections are logical mapping between endpoints and RTP/UDP/IP streams.

SS7 is the traditional common channe signaling protocol.
ISUP is an application protocl to setup and tear down connections. The path of a connection can be different from the path of signaling.
SIGTRAN, Signaling Transport has the objective of transporting SS/ signaling over IP. Problems: address translation, message incapsulation, transport over IP (both UDP and TCP are not good solutions for the transport of SS7 over ip, so it has been developed SCTP), interworking MGC/SG.
SCTP, Stream Control Transport Public provides a reliable transport for signaling interworking. It has been developed because TCP is not reliable enough for SIGTRAN.
