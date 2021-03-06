.. _lsp_support:

LSP Support
===========

See the `Language Server Specification`_ for details.

+-------------------------+---+-------------------------------------+
| Feature                 |   |                                     |
+=========================+===+=====================================+
| Completion              | ✔ | See :ref:`completion`               |
+-------------------------+---+-------------------------------------+
| Hover                   | ✔ |                                     |
+-------------------------+---+-------------------------------------+
| Signature Help          | ✔ |                                     |
+-------------------------+---+-------------------------------------+
| Goto Declaration        | ✔ |                                     |
+-------------------------+---+-------------------------------------+
| Goto Type               | ✔ |                                     |
+-------------------------+---+-------------------------------------+
| Goto Implementation     | ✔ |                                     |
+-------------------------+---+-------------------------------------+
| Find References         | ✔ | [#references]_                      |
+-------------------------+---+-------------------------------------+
| Document Highlight      | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Document Symbol         | ✔ | For structural elements             |
+-------------------------+---+-------------------------------------+
| Code Action             | ✘ | Supported by RPC [#rpc]_ [#code]_   |
+-------------------------+---+-------------------------------------+
| Code Lens               | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Document Link           | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Document Color          | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Color Presentation      | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Formatting              | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Range Formatting        | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Rename                  | ✘ | Supported by RPC [#rpc]_ [#rename]_ |
+-------------------------+---+-------------------------------------+
| Folding/Selection Range | ✘ |                                     |
+-------------------------+---+-------------------------------------+
| Diagnostics             | - | Provided by extensions [#static]_   |
+-------------------------+---+-------------------------------------+

.. _Language Server Specification: https://microsoft.github.io/language-server-protocol/specification

.. [#rpc] Available through RPC (i.e. non-LSP client) LSP support should be added soon.
.. [#code] Code actions translate to :ref:`refactoring` actions in Phpactor, and should be available in the next release.
          added soon.
.. [#references] For class like references, functions and member accesses (static and object instances)
.. [#rename] RPC supports :ref:`refactoring_rename_variable`, :ref:`refactoring_rename_class`, :ref:`refactoring_rename_member`,
.. [#static] For example PHPStan https://github.com/phpactor/language-server-phpstan-extension
