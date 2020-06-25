---


---

<h1 id="multimedia-internet--part-2">Multimedia Internet  part 2</h1>
<h2 id="mobile-telephony-quality-90s-vs-mobile-telephone-quality-now">Mobile telephony quality 90s VS mobile telephone quality now</h2>
<p>Mobile telephony quality in the 90s was equal and, in some cases, better than the quality we have now. There are various reason for that:</p>
<ul>
<li><strong>Handset design:</strong> phone today’s main focus is not voice quality, so the speaker and the microphone can be misplaced, for example they can be very near. <em>Solution:</em>  using multiple microphones.</li>
<li><strong>Sharp background noise:</strong> background noise is filtered, but when it comes to sudden sounds can be difficult to eliminate them. <em>Solution:</em> using specialized headsets with noise cancelling technology.</li>
<li><strong>Phone to tower connection:</strong> the distance from a cellular tower can degrade the quality of a voice call. <em>Solution:</em> signal booster for telephones.</li>
<li><strong>Voice data conversion:</strong> cellular voice phone calls can be compressed and unpacked various times, degrading the voice quality. <em>Solution:</em> VoLTE can compress the voice signal only once.</li>
</ul>
<blockquote>
<p><strong>VoLTE:</strong> it is a solution on the network side, where we give voice packets a better treatment respect to other type of packets to limit their delay.</p>
</blockquote>
<h2 id="carrier-grade-ip-telephony-vs-internet-telephony">Carrier Grade IP telephony vs internet telephony</h2>
<p>In carrier grade IP telephony the telephony service is provided by telco operators. There is a specific resource reservation for carrier grade telephony, so the quality is good.<br>
Internet telephony uses the public internet like Skype: the quality is worse than carrier grade.  Interconnections between aAS are bottleneck that delays packets and decreases quality. For telephony packets a delay is equivalent to a packet loss, and a losing a packet is noticed by users and degrade the quality of the call. The packets with too much delay are simply dropped. We can’t threat packets from telephony and packets from other applications equally. A very large speed alone is not enough to guarantee strictly QoS, but we need to combine it with good traffic management for example giving VOIP buffer more priority over the data buffer.</p>
<h2 id="net-neutrality">Net neutrality</h2>
<p>The approach is to not differentiate services on user identity, but to differentiate them based on which type of application the packets are from. E.g. VOIP buffer has priority over data buffer.</p>
<p>Business in the internet is regulated by rules and laws that have technical consequences. The debate has been centered around policy, law and finance as if the network was a given thing, but it is not.</p>
<h2 id="ip-interconnection">IP interconnection</h2>
<p>The internet is a collection of networks called Autonomous Systems, that are administered by independent entities. The interconnection between two AS is a private contract between the two administrators. Usually traffic across interconnection interfaces is treated as best effort.</p>
<ul>
<li><strong>Transit:</strong> between a larger AS and a smaller one, and it is payed for.</li>
<li><strong>Peering:</strong> the ASs have similar size. Is the preferred choice when possible because they don’t have to pay each other or pay very little respect to transit. It is not transitive.</li>
</ul>
<p>In this scenario there are various players:</p>
<ul>
<li><strong>Tier 1 operator:</strong> can reach every IP address in the world without buying transit services, but just with its network or peering contracts, e.g. AT&amp;T, Verizon, Detusche Telekom, Sparkle, Telefonica.</li>
<li><strong>Over The Top Providers (OTTP):</strong> e.g. Google, they are service provider that can reach people and businesses all over the world without a network.</li>
<li><strong>Content Provider:</strong> e.g. Netflix, they are a problem for Telcos because there’s gonna be more content with pay per view requested by users without generating more money for the Telco, but only adding expense to them.</li>
<li><strong>Service Provider:</strong> provides internet access to users.</li>
<li><strong>Content Delivery Network (CDN):</strong> a system of computers connected to the internet that distributes content such as audio and video.</li>
</ul>
<blockquote>
<p>A <strong>cache</strong> is a server that can store a content while it is transiting. They are placed in strategical points where the traffic is more intense. If a content is highly requested is convenient to store it in the cache. Caches can be place at high or low hierarchical level. Some advantages are: performance and quality and reducing the transit diminishing costs. They have inside them the <strong>Content Database</strong>.</p>
</blockquote>
<h2 id="next-generation-network-ngn">Next Generation Network (NGN)</h2>
<p>In the traditional access network all the links are made of copper apart the links between the Central Office (CO) and the Service Distribution Frame (SDF), which is fiber. The copper links have a series of disadvantages respect to the fiber:</p>
<ul>
<li>collect more external noise</li>
<li>create more natural interferences</li>
<li>degradation due to humidity</li>
<li>narrower (smaller) bandwidth</li>
</ul>
<p>NGN is not simply a substitution of copper with fiber, also the architecture of the access network changes.</p>
<ul>
<li><strong>FTTE</strong>, Fiber To The Exhchange: very simple cabinets who don’t need power because they are all mechanical electrical (no electronics). They are cheap, they need low manteinance and are unnoticed by people. Not very interesting.</li>
<li><strong>FTTC</strong>, Fiber To The Cabinet: they have lot of problems because the technology is mixed (optical and electronics), and it requires advanced tech that consumes power and occupies a large space (vandalism is possible). The street cabinet needs electrical power, and they also need air conditioning.</li>
<li><strong>FTTB</strong>, Fiber To The Building: the Service Distribution Frames (SDF) are all optical (passive) and underground (small). There are some issues similar to the FTTC street cabinet, but they are inside the building so vandalism is less of a problem and they have an easy life in accessing power.</li>
<li><strong>FTTH</strong>, Fiber To The Home: all the connections from the Central Office (CO) to the house are passive. It is possible to have the same speed in uplink and in downlink. The main problem is that the deployment is complicated because it is difficult to pass the fiber form the sidewalk to the basement of the building.</li>
</ul>
<blockquote>
<p>There are two types of FTTH:</p>
<ul>
<li><strong>P2P</strong>, Point To Point: there is a dedicated fiber to each user.</li>
<li><strong>PON</strong>, Passive Optical Network: a tree structured network of fibers where the capacity of the fiber is shared among users. Only passive devices are used. The main advantage is the cost, while the disadvantages are the performance (bandwidth shared among users), and the privacy.<br>
<em>TDM-PON</em>, Time Division Multiplexing: it separates uplink and downlink through wave division. <em>Shared PON:</em>  easier to assign users to operators, and also sharing an infrastructure diminishes costs for the operators.</li>
</ul>
</blockquote>
<h1 id="unbundling-and-colocation">Unbundling and colocation</h1>
<p>Operations of changing an operator; they are mandatory and cannot be refused. They are usually done in strategical points for example between cabinets.<br>
The cost of this operation varies depending on where you change operator:</p>
<ul>
<li><strong>Unbundling:</strong> the closest to the final user, the cheapest. The closest to the CO, the highest price.</li>
<li><strong>Colocation:</strong> substituting one operator in the Optical Line Terminal (OLT) that is inside the CO.</li>
</ul>
<blockquote>
<p><strong>OLO,</strong> Other Licensed Operators: new operators that are not former state company (<strong>incumbent operators</strong>).</p>
</blockquote>
<h1 id="business-issues-for-operators">Business issues for operators</h1>
<p>The deployment of the NGAN must be balanced between costs for the operatore and average money that the user will pay. The costs are not uniform, and they depend on the kind of territory:</p>
<ul>
<li><strong>Metropolitan</strong> areas: the deployment cost per user is low since the population density is high, and the costs are likely to be repayed by the costumers.</li>
<li><strong>Suburban</strong> areas: middle costs and middle payment from the costumers between the two other cases.</li>
<li><strong>Rural/mountain</strong> areas: from a business POV they are not convenient, because the population is sparse and the difficulties for deploying the fiber are high. In this case the state get involved contributing to the investment to permit even the people that live in less dense places to have NGAN.</li>
</ul>
<h1 id="services-of-operators">Services of operators</h1>
<p>In a Next Generation Access Network (NGAN) the services provided are:</p>
<ul>
<li><strong>intermediate service:</strong> a typical example is the connection of mobile network antennas to the core network aka <em>backhauling</em>. Another example is the tube rental, where an operator rents tube to other operators.</li>
</ul>
<blockquote>
<p>Various solutions for backhauling:</p>
<ul>
<li>E1 lines for backhauling, not the best way because we have to mantain two different systems.</li>
<li>GPS: the signal is stable enough, but it is not the best idea because the GPS system is property of the USA, and they can decide to turn it off at any moment.</li>
<li>Pseudowire: the PW packets will be characterized by a guaranteed SLA, while other packets will have a statistical SLA.</li>
</ul>
</blockquote>
<ul>
<li><strong>wholesale service:</strong> inter-operator services like wholesale line rental, wholesale leased line, unbundling, colocation. Wholesale services are not traded in single units, but in large stocks.</li>
<li><strong>retail service</strong></li>
</ul>
<p>The basic requirements for operators to trade this kind of services are that the QoS must be negotiable both at the connection setup and when the connection is established, and there is also have to be a minimal list of voice, audio and video coders that should be supported.</p>
<h1 id="telephony-over-ip-toip">Telephony Over IP (TOIP)</h1>
<p>IP telephony is a replacements for Plain Old Telephone Service (POTS). It has to have some services possible:</p>
<ul>
<li>numbering plan must be preserved</li>
<li>lawful interception must be guaranteed</li>
<li>malicious call identification must be possible</li>
<li>anonymous call rejection must be possible</li>
<li>interoperability with POTS guaranteed</li>
</ul>
<p>Is TOIP a full replacement of POTS? Not really.</p>
<h1 id="multimedia-streaming">Multimedia streaming</h1>
<p>It is the distribution of audio and video content. The content is consumed during its transfer.</p>
<blockquote>
<p>Two main flavors:</p>
<ul>
<li><strong>PUSH:</strong> provider distributes contents based on a time schedule.</li>
<li><strong>PULL:</strong> users can ask for any content any time, it has higher costs and it is more difficult caching and multicasting.</li>
</ul>
</blockquote>
<p>The chain of the service stream is composed by:</p>
<ul>
<li>DB, where is stored the content</li>
<li>server</li>
<li>coder, to make the content format compatible with network transportation</li>
<li>network</li>
<li>playout buffer</li>
<li>playout service</li>
</ul>
<p>The media transfer is unidirectional form the server to the client.<br>
The control informations (<em>signaling</em>) on the control plane are bidirectional, and they are used to set up the connection, to negotiate the media, to get quality feedback in real time, to interact with the playout and to tear down the connection.</p>
<ul>
<li>Streaming <strong>unicast:</strong> one distribution flow per user; total bandwidth required.</li>
<li><strong>Caching:</strong> caches store contents and they replay stored content for new users requiring them; smaller bandwidth require. It can be done at different levels: higher is closer to the interconnection, lower is closer to the user.</li>
<li><strong>Proxy server:</strong> owned and managed by the Service Provider (SP).</li>
<li>Streaming <strong>multicast:</strong> ideal way of streaming the media, using multicast distribution. It is hard to use because most network do not support multicasting (IP for example, it has a primitive multicasting capacity adn cannot support high bandwidth services).</li>
</ul>
<h1 id="internet-protocols">Internet protocols</h1>
<p>Internet protocols are the structure and the format of messages. They are normally client-server protocols, where a client sends a request to a server, and the server replies with a response. The ones we are interested in are:</p>
<ul>
<li>HTTP (HyperText Transfer Protocol): plaintext, not encrypted</li>
<li>HTTPS: information is encrypted</li>
<li>SIP, RTSP: specific for signaling</li>
</ul>
<p>A typical HTTP request message has the following structure:</p>
<blockquote>
<p>request line \r\n<br>
header line 1\r\n<br>
header line 2\r\n<br>
…<br>
header line n\r\n<br>
\r\n<br>
body</p>
</blockquote>
<p>The first line and the header lines are text strings, and they are separated by the <em>line separator</em> \r\n. The additional line separator after the last header line marks the start of the body of the message. There is no line terminator after the last byte of the body, so the <strong>content length header</strong> is fundamental because it identifies univocally the last byte of the current message.</p>
<p>The <strong>request line</strong> (first line of the message) has the following structure:</p>
<blockquote>
<p>method request-uri protocol-version</p>
</blockquote>
<p>It has three fields separated by a single space character. The first one is the method, that specifies the kind of action that the requesting entity would like to perform. The second field specifies which is the resource on which the action must be performed, and the third field which specifies the protocol identity and version.<br>
Example:</p>
<blockquote>
<p>GET /serviceA?parameter=n_request HTTP/1.1</p>
</blockquote>
<p>The second parameter is partial, the complete one can be for example:</p>
<blockquote>
<p><a href="http://myservice.com/serviceA?parameters.required=n_requests">http://myservice.com/serviceA?parameters.required=n_requests</a></p>
</blockquote>
<p>If the <strong>Universal Resource Identifier (URI)</strong> starts with http:// it means that we are using the HTTP protocol.<br>
The name of the headers are standardized. The headers are divided into four categories:</p>
<ul>
<li><strong>general headers:</strong> provide details on the connection between the server and the client. It can be connection: close or connection: keep alive.</li>
</ul>
<blockquote>
<p>There are two main way to establish and maintain a connection. In the first case for every request a connection is established and closed. In the second case we maintain a connection for multiple requests, a more efficient way to use a connection with latency diminishing and throughput improving. In the second case we can also use <strong>pipeline:</strong> the client sends requests even if it has not received the responses of the previous messages. In this way we can improve a lot the throughput.</p>
</blockquote>
<ul>
<li><strong>request headers:,</strong> there are various methods: GET, PUT POST, POST (to make a complicated request), DELETE.</li>
<li><strong>response headers,</strong> same structure of a request message, but it can use some headers that are not used by request messages, for example HTTP/1.1 200 OK.</li>
<li><strong>entity headers:</strong> information about the content carried in the body of the message, for example the content_length header that indicates how many bytes the content is long and when start considering the next packet.</li>
</ul>
<p>The <strong>body</strong> is a sequence of bytes, and it can carry any kind of content: a text, a picture, a video clip, json file… It is <em>byte clean</em>, meaning that any value is allowed since there is no interpretation of byte value.</p>
<h1 id="https">HTTPS</h1>
<p>HyperText Transfer Protocol over Secure Socket Layer<br>
Respect to HTTP adds encryption to the data transfer. In plain HTTP the structure is, starting from the bottom, TCP, HTTP without encryption. In HTTPS the architecture is TCP, TLS (Transport Layer Security), HTTP. TLS can be certificate based (the most common) or Private Shared Key (PSK) based, that is faster, but in which the key is usually not exchanged through the network.</p>
<h1 id="rtsp">RTSP</h1>
<p>Real Time Streaming Protocol<br>
Fully integrated with other important internet protocols such that: HTTP, SDP (Session Description Protocol), RTP (Real Time Protocol). Gives features such: start, pause, jump, fast forward, fast reverse.</p>
<p>Example: an user’s terminal wants a video/audio content. The exchange messages will be with two logically separated entities.</p>
<ul>
<li>
<p>client to web server<br>
GET /mission_to_mars.SDP HTTP/1.1</p>
</li>
<li>
<p>web server to client<br>
http/1.1 200 OK<br>
Content_type: application/SDP<br>
Content_length: xxx<br>
…<br>
m=audio RTP/AVP 0<br>
a=control:rtsp://audio.source.come/mission_to_mars/audio<br>
m=video RTP/AVP 32<br>
a=control:RTSP://video.source.com/mission_to_mars/video</p>
</li>
<li>
<p>RTSP, client request to the media server<br>
SETUP RTSP/AVP/UDP;unicast;client_port=3056-3057</p>
</li>
<li>
<p>audio server responds to client<br>
rtsp/1.0 200 OK<br>
transport: RTP/AVP/UDP;unicast;client_port=3056-3057;server-PORT=5000-5001</p>
</li>
<li>
<p>client to video server<br>
SETUP rtsp://video.source.com/mission_to_mars/video rtsp/1.0<br>
transport: RTP/AVP/UDP;unicast;client_port=3058-3059</p>
</li>
<li>
<p>video server to client<br>
rtsp/1.0 200 OK<br>
transport: RTP/AVP/UDP;unicast;client_port=3058-3059;server_port=5002-5003</p>
</li>
<li>
<p>client sends play request to audio server<br>
PLAY rtsp://audio.source.com/mission_to_mars/audio rtsp/1.0</p>
</li>
<li>
<p>audio server responds<br>
rtsp/1.0 200 OK</p>
</li>
<li>
<p>client sends play command to video server<br>
PLAY rtsp://video.source.com/mission_to_mars/video rtsp/1.0</p>
</li>
<li>
<p>video server answers<br>
rtsp/1.0 200 OK</p>
</li>
</ul>
<h1 id="video-server">Video server</h1>
<p>System for streaming, started in the 1990s has not a lucky beginning. There are a lot of parameters that should be taken into account:</p>
<ul>
<li>Storage: video files occupies a very large storage space. We need to consider how many contents do we have and how much do they weight. One way to store lot of contents without spending too much money is to use Redundant Array of Inexpensive Disks (RAID). <strong>Replication factor:</strong> how many times we have stored a content, it determines its reliability.</li>
</ul>
<blockquote>
<p>There are two main types of hard drives: HDD that are rotational drivers, are slow, but not much expensive and SDD solid state that are much faster, but also more expensive.</p>
</blockquote>
<ul>
<li>speed of loading the content</li>
<li>access time</li>
<li>cost</li>
</ul>
<p>The <strong>long tail graph</strong> put in relation the <strong>hit rate</strong> (how many people watches each content) with the number of contents.<br>
We can divide the CPs into two main categories depending of their hit rate:</p>
<ul>
<li><strong>High hit rate:</strong> left side of the graph, with smaller number of contents, high definition, large storage for each content, payed service, require Ultra Large Bandwidth (ULB) network access, acquisition of content is expensive. IPTV.</li>
<li><strong>Long tail:</strong> right side of the graph, with large number of contents, low definition, small storage space for each content, free service, doe not require ULB, acquisition of content is mainly free. Internet TV.</li>
</ul>
<h1 id="media-formats">Media formats</h1>
<p>A digital video is a sequence of images. The frequency of those images is called <strong>frame rate</strong>. Standard FPS are between 25 and 40, but 8k has more than 100 FPS (UHD). The typical resolution is 1280x720 for HD, 1920x1080 for FULL-HD, that are pixels x pixels. A pixel is a colored dot.<br>
Color spaces:</p>
<ul>
<li><strong>RGB:</strong> it defines the amount of Red, Green and Blue in each pixel</li>
<li><strong>YCrCb:</strong> amount of Y luminance (<em>luma</em>, the most important), Cr red and Cb blue (the lasts two indicator are called <em>chroma</em>). The sampling can be configured in various ways: 4:4:4 is fully sampled, 4:2:2 has less information (the chroma components are halved) so it occupies smaller storage and uses less bandwidth and 4:2:0 where the most dominant characteristic is the luminance which is transmitted every pixel, while the chroma are distributed in 4 pixels each.</li>
</ul>
<p>The bit rate for transmitting a FULL HD video is too high if the media is not compressed. The formats for storage are different from the formats for transmission. An optimized way to compress video files is compression by prediction that works in most of cases, with some exceptions ( first scene of “Silence of the lamb”).</p>
<h1 id="video-formats">Video formats</h1>
<p>There is no optimal video format for all cases, there is always a trade off between quality and bandwidth. Video files are made of 2 parts:</p>
<ul>
<li><strong>Container:</strong> that is how the file, metadata and data are structured. It contains the metadata and the compressed video data encoded using the codec. Generally is called the <em>format</em>, because it reflects the file’s extension.</li>
<li><strong>Codec:</strong> is the protocol for encoding and decoding the video.</li>
</ul>
<h1 id="iptv-and-internet-tv">IPTV and Internet TV</h1>
<p>The IPTV (Internet Protocol Television) is a high quality service distribution of digital TV using both dedicated network infrastructure and public internet. The Internet TV is the distribution of the media through the public internet usually with low quality, but smaller bit rate.<br>
IPTV is a linear/push type of content distributor: its programs transmission is scheduled; it can also have an archive with older content, so it can also be a pull type content provider. Internet TV is a non linear/pull type: users ask for a specific content whenever they want.<br>
The users in the IPTV are known and registered and they are authenticated usually with a set of box + smart card, while in the Internet TV the user can be anyone. IPTV is a payed service while Internet TV is free. IPTV has high quality contents while Internet TV have web based content. Contents in IPTV are protected, while contents in Internet TV are not.</p>
<h1 id="peer-to-peer-p2p-video-streaming">Peer-to-peer (P2P) video streaming</h1>
<p>We are not gonna study the underlay topology aka the physical layer that can be very long. We focus on the overlay topology that is virtual and build by the nodes autonomously since those two topologies are usually independent one from another. There are three main overlay topologies: <strong>tree</strong> hierarchical topology, single point of failure, <strong>forest</strong> that is made by multiple trees interconnected and resolves the single point of failure problem and <strong>mesh</strong> where a leave event might be unnoticed. Tree and forest topologies are hierarchical, while the mesh topology is a generic one not hierarchical.<br>
There are also some performance issue with the tree and the forest topology. If the depth of a tree grows too much, the last leafs of are gonna have high delay and packet loss respect to high level nodes. So this type of topologies are particularly effected by the depth of trees, so deep trees should be avoided, but it was not possible to do so until a few years ago (ADSL era, limit on uplink). Wide trees should be preferred.</p>
<p>Construction of topology for tree and forest topologies:</p>
<ul>
<li><strong>join:</strong> when a node wants to join a network.</li>
<li><strong>rejoin:</strong> when a node becomes an orphan (the node at which it is connect leave) and it must rejoin the network.</li>
</ul>
<p>In mesh topology the join and rejoin operations are more complicated, but it can guarantee more performance and stability. Every peer has its own <strong>Buffer Map</strong> (BM) used to keep record of the segments it has received. The peers exchange periodically their BM, and each node builds and maintains in real time the m cache that is a matrix composed by all the BM of the other nodes. When a node needs a segment of a media it knows which peer have it. This type of topology is robust to leave event. The main problem is when a node has too few neighbors. There is an optimal number of neighbors a node should have to not have too many BM exchanges or too less peers to ask for content.</p>
<p><strong>Node selection:</strong> when a node is joining or rejoining a network, it has to take into account various metrics such as <em>ping time</em> .</p>
<p>For tree and forest topologies joining close to the root is better than joining at a leaf, but the competition is stronger. The system might keep track of the stability of a peer, so that the join/rejoin operation close to the root can e done only to high stable peers.</p>
<h1 id="sip-session-initiation-protocol">SIP: Session Initiation Protocol</h1>
<p>SIP is a signaling protocol. It handles the set up, tear down and management of IP multimedia sessions. It is naturally integrated with other internet protocols such that SDP, RTSP and SAP (Session Announcement Protocol). SIP usually adopts RTP as a transport for media streams.</p>
<p>SIP is a client/server protocol:</p>
<ul>
<li><strong>Client:</strong> called User Agent Client (UAC), is in the user’s device, sends SIP requestes.</li>
<li><strong>Server:</strong> there are four types of server proxy, registrar, redirect, User Agent Server (UAS). The last one is in the user’s device and receives SIP requests.</li>
</ul>
<p><strong>Registrar server:</strong> it handles SIP registration requests. Those requests are used by devices to register into the SIP network and they are mandatory for any device.</p>
<p><strong>Basic call:</strong></p>
<ul>
<li>INVITE message</li>
<li><em>Ringing</em>, a PRES (Provisional Response) send back to the caller to signal him that the device of the called user is ringing</li>
<li>OK,  response to signal that the call has been accepted and it has been set up</li>
<li>ACK-OK</li>
<li>BYE, request when someone hungs up the call</li>
<li>OK</li>
</ul>
<p><strong>Transaction:</strong> a software object that describes the session and in particular its phases.<br>
<strong>Provisional Responses:</strong> are used to let the transaction knows that the request is being processing. PRES are never final, they don’t mean that the request has been fully processed. For example in case of long requests the client must know that the request is in processing, so PRES messages are sent periodically from the server to the client to keep the client updated so that he will keep waiting the final response. Sending periodic provisional responses makes the TCP keep the connection alive. This is a problem we don’t have with UDP because UDP has no connection.</p>
<p><strong>SIP messages:</strong> they can be wither requests or responses. SIP has been one of the first signaling protocol to have textual format messages as opposed to traditional signaling protocols in which they are binary. This is usually an advantages even if textual messages consume more bandwidth.<br>
The <em>request line</em> specifies the type of request and its parameters.<br>
<strong>Body</strong> of SIP messages: can carry almost everything, it is not standardized like the body of HTTP. The most frequent body is application/SDP that is used for the navigation of the media.<br>
E.g. for a SIP address: <a href="mailto:diego@home.com">diego@home.com</a></p>
<p><strong>SIP request methods:</strong></p>
<ul>
<li>invite, to start a session</li>
<li>bye, to close a session</li>
<li>register, to register a user in the SIP network</li>
<li>ack, acknowledge</li>
<li>options,</li>
<li>cancel, to cancel a signaling transaction</li>
</ul>
<p>Request:</p>
<blockquote>
<p>method request URI version\r\n</p>
</blockquote>
<p>Response:</p>
<blockquote>
<p>version statuscode reason phrase\r\n</p>
</blockquote>
<p>Status code is three digit:</p>
<ul>
<li>1XX: provisional</li>
<li>2XX: success, the most important is 200 OK</li>
<li>3XX: redirection</li>
<li>4XX: bad request failure, the request message is not well formed. E.g. 404 not found: the resource has not been found</li>
<li>5XX: server failure</li>
<li>6XX: global failure</li>
</ul>
<p>All messages have <strong>headers:</strong></p>
<ul>
<li>General: (to, from, call ID) is a triplet specific of SIP that identifies called and calling users.</li>
<li>Request: only used for requests.</li>
<li>Response: only used for responses.</li>
<li>Entity: their main purpose is to describe the content of the message body.</li>
<li>VIA: specifies the SIP route followed by the request message, so that response can use the same path backwards. The response must follow the same path backwards because proxies are generally stateful: they remember the dialogues of the messages that they forward, so via headers are used to guarantee that the SIP path of responses is the backward path of requests.</li>
</ul>
<h1 id="session-description-protocol-sdp">Session Description Protocol (SDP)</h1>
<p>SDP is used for the description of the format of media streams. For each media stream of a session, an SDP description is needed. SDP descriptions are carried in the body of SIP messages and they enable <em>media negotiation</em>.<br>
Media negotiation happens with a two way handshake, and it is very simple compared to the media negotiation of previous signaling protocols like H.323.</p>
<blockquote>
<p>Note that SDP does not transport media: it is used only for their description.</p>
</blockquote>
<h1 id="signaling-interworking">Signaling interworking</h1>
<p>The goal is to make different signaling protocols interoperate, that is one of the most complex problems of telephony. The two main problems are in the control plane where we use different signaling protocol and in the user plane where we have different media formats. The signaling protocols that we consider are H.323, SS7 (traditional signaling protocol of the public switched telephone network) and SIP.</p>
<p><em>Media gateways</em> translate the media, while <em>signaling gateways</em> translate the signaling.<br>
Media gateways are controlled by <strong>Media Gateway Controllers (MGC)</strong> and they communicate using a specialized signaling protocol such as the <strong>Media Gateway Control Protocol (MGCP)</strong>. MGCs and signaling gateway aka MGCP need to intercommunicate, so a gateway architecture is created.</p>
<p><strong>Soft switch</strong> is a distributed system for interworking that manages separately media and signaling. MGCs intercommunicate through SIP. MGCs communicate with media gateways with MGCP.<br>
MGC specifies how a media gateway must translate media, and can require dynamic change of media format.<br>
The basic objects managed by MGCP are the endpoints. MGCP connections are logical mapping between endpoints and RTP/UDP/IP streams.</p>
<p>ISUP is an application protocol to setup and tear down connections. The path of a connection can be different from the path of signaling.</p>
<p>SIGTRAN, Signaling Transport has the objective of transporting SS7 signaling over IP. Problems: address translation, message incapsulation, transport over IP (both UDP and TCP are not good solutions for the transport of SS7 over ip, so it has been developed SCTP), interworking MGC/SG.<br>
SCTP, Stream Control Transport Public provides a reliable transport for signaling interworking. It has been developed because TCP is not reliable enough for SIGTRAN.</p>

