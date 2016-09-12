# UniBs-State_Machine_Executor-ns3_full

In this project we have put forward a mechanism that can greatly enhance the flexibility of
Layer-4 protocols running on a network node. We implemented an extended finite state
machine executor in ns-3 that can flexibly deploy Layer-4 protocols using their own software-
defined state machines. It allows each protocol to be run-time programmed, thus eliminating
the need for a reboot or even recompilation of the kernel to switch to a different protocol. The
mechanism seems similar to the Software-defined networking approach, but being slightly
different with its implementation on the upper layers of the stack. For a long time, although
Transport Layer protocols have been designed and represented using state machines , they
have nevertheless been implemented in a hard-wired way. The current TCP implementation is
fixed, and requires a kernel reboot or even recompilation to switch to a different TCP flavour.
The executor that we have developed solves this problem through flexibly deploying different
Layer-4 protocols on-the-fly, by simply loading a protocol’s state machine into the state
machine executor. The state machines can be programmed effortlessly by a user as they are
written using XML, and can then be parsed by the executor using libxml2. Moreover, the
executor implementation allows users to design and implement new Transport protocols or
make modifications to the existing protocols without having to making any changes to the
original source code. All that is required is to describe the state transition table of a protocol
which includes the involved states, events and actions, and then simply load it onto the
executor at run-time. Another special feature of the executor is that it allows for the flexible
manipulation of congestion window in real time. This enhances adaptability by allowing the
window to evolve based on some user-defined rules that can greatly improve the performance
of a protocol as per the changing network conditions. The executor implementation in a real
Linux kernel, based on the extended finite state machine concept provided in this thesis has
been left as future work.

For a detailed explanation of the project refer to - [State_Machine_Executor Report](https://drive.google.com/open?id=0B-jpEEacF1bna2xZbUctS2ZJRzQ)
