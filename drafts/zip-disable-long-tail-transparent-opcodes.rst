::

  ZIP: XXX
  Title: Disable Longtail Transparent Opcodes
  Owners: Deirdre Connolly <deirdre@zfnd.org>
  Status: Draft
  Category: Consensus
  Created: 2019-08-12
  License: MIT


Terminology
===========

The key words "MUST" and "MAY" in this document are to be interpreted as described in
RFC 2119. [#RFC2119]_

The term "network upgrade" in this document is to be interpreted as described in ZIP 200
[#zip-0200]_.

The term "Sapling" in this document is to be interpreted as described in ZIP 205
[#zip-0205]_.

Abstract
========

This proposal disables numerous opcodes that see little to no usage,
and therefore reduces complexity and increases maintainability for any
implementations of Zcash.

Motivation
==========

Data collected by str4d:

::

89297: OP_2 <data:33> <data:33> <data:33> OP_3 OP_CHECKMULTISIG
6802: OP_2 <data:33> <data:33> OP_2 OP_CHECKMULTISIG
94: OP_1 <data:33> <data:33> OP_2 OP_CHECKMULTISIG
34: OP_IF <data:4> OP_CHECKLOCKTIMEVERIFY OP_DROP <data:33> OP_CHECKSIG OP_ELSE OP_HASH160 <data:20> OP_EQUALVERIFY <data:33> OP_CHECKSIG OP_ENDIF
8: OP_2 <data:65> <data:65> <data:65> OP_3 OP_CHECKMULTISIG
7: OP_2 <data:33> <data:33> <data:33> <data:33> <data:33> OP_5 OP_CHECKMULTISIG
7: OP_IF <data:4> OP_CHECKLOCKTIMEVERIFY OP_DROP <data:33> OP_CHECKSIG OP_ELSE OP_SIZE 20 OP_EQUALVERIFY OP_HASH160 <data:20> OP_EQUALVERIFY <data:33> OP_CHECKSIG OP_ENDIF
6: OP_IF <data:4> OP_CHECKLOCKTIMEVERIFY OP_DROP <data:33> OP_CHECKSIG OP_ELSE OP_SHA256 <data:32> OP_EQUALVERIFY <data:33> OP_CHECKSIG OP_ENDIF
6: OP_2 <data:33> <data:33> <data:33> <data:33> OP_4 OP_CHECKMULTISIG
5: <data:33> OP_CHECKSIG
2: OP_SHA256 <data:32> OP_EQUAL
2: OP_3 <data:33> <data:33> <data:33> <data:33> <data:33> OP_5 OP_CHECKMULTISIG
2: OP_3 <data:65> <data:65> <data:65> <data:65> <data:65> <data:65> <data:65> OP_7 OP_CHECKMULTISIG
2: OP_1 <data:33> OP_1 OP_CHECKMULTISIG
2: OP_IF OP_SIZE 20 OP_EQUALVERIFY OP_SHA256 <data:32> OP_EQUALVERIFY OP_DUP OP_HASH160 <data:20> OP_ELSE <data:4> OP_CHECKLOCKTIMEVERIFY OP_DROP OP_DUP OP_HASH160 <data:20> OP_ENDIF OP_EQUALVERIFY OP_CHECKSIG
1: OP_IF OP_SHA256 <data:32> OP_EQUALVERIFY OP_DUP OP_HASH160 <data:20> OP_ELSE OP_1 OP_DROP OP_HASH160 <data:20> OP_ENDIF OP_EQUALVERIFY OP_CHECKSIG
1: OP_IF OP_SHA256 <data:32> OP_EQUALVERIFY OP_DUP OP_HASH160 <data:20> OP_ELSE <data:2> OP_CHECKLOCKTIMEVERIFY OP_DROP OP_DUP OP_HASH160 <data:20> OP_ENDIF OP_EQUALVERIFY OP_CHECKSIG
1: OP_IF OP_SHA256 <data:32> OP_EQUALVERIFY OP_DUP OP_HASH160 <data:20> OP_ELSE <data:3> OP_CHECKLOCKTIMEVERIFY OP_DROP OP_DUP OP_HASH160 <data:20> OP_ENDIF OP_EQUALVERIFY OP_CHECKSIG
1: OP_IF OP_HASH160 <data:20> OP_EQUALVERIFY OP_DUP OP_HASH160 <data:20> OP_ELSE <data:4> OP_CHECKLOCKTIMEVERIFY OP_DROP OP_DUP OP_HASH160 <data:20> OP_ENDIF OP_EQUALVERIFY OP_CHECKSIG
1: OP_IF <data:4> OP_CHECKLOCKTIMEVERIFY OP_DROP OP_SIZE 20 OP_EQUALVERIFY OP_HASH160 <data:20> OP_EQUALVERIFY <data:33> OP_CHECKSIG OP_ELSE OP_SIZE 20 OP_EQUALVERIFY OP_HASH160 <data:20> OP_EQUALVERIFY <data:33> OP_CHECKSIG OP_ENDIF
1: OP_1 <data:33> <data:33> <data:33> OP_3 OP_CHECKMULTISIGVERIFY OP_2 <data:33> <data:33> OP_2 OP_CHECKMULTISIG
1: OP_2 <data:33> <data:33> <data:33> <data:33> <data:33> <data:33> OP_6 OP_CHECKMULTISIG
1: OP_2 <data:33> <data:33> <data:33> OP_3 OP_CHECKMULTISIGVERIFY <data:4> OP_DROP OP_DEPTH OP_0 OP_EQUAL
1: <data:33> OP_CHECKSIGVERIFY OP_0 OP_DROP OP_DEPTH OP_0 OP_EQUAL


Conventions
===========

Lorem ipsum.

Specification
=============

Consensus rules
---------------

Lorem ipsum.

Rationale
=========

Lorem ipsum.

Security and Privacy Considerations
===================================

Lorem ipsum.

References
==========

.. [#RFC2119] `Key words for use in RFCs to Indicate Requirement Levels <https://tools.ietf.org/html/rfc2119>`_
.. [#zip-0200] `ZIP 200: Network Upgrade Activation Mechanism <https://github.com/zcash/zips/blob/master/zip-0200.rst>`_
.. [#zip-0205] `ZIP 205: Deployment of the Sapling Network Upgrade <https://github.com/zcash/zips/blob/master/zip-0205.rst>`_
