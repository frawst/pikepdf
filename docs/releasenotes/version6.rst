v6.2.6
======

- Rebuild binary wheels for certain platforms they were blocked from release by lxml not releasing compatible wheels.
Mainly Windows.

v6.2.5
======

- Rebuild binary wheels using qpdf 11.2.0.

v6.2.4
======

- Removed a debug message during mmap.

v6.2.3
======

- Fixed errors when using AccessMode.mmap. Thanks @zachgoulet.

v6.2.2
======

- Fixed noisy log message.
- Made some flakey tests less flakey.
- Fixed deprecated information in setup.cfg. Thanks @mgorny.

v6.2.1
======

- Rebuild binary wheels using zlib 1.2.13. Source build unchanged.

v6.2.0
======

- Add new keyword argument ``Pdf.save(..., deterministic_id=True)`` for saving
  bit-for-bit reproducible PDFs. Thanks @josch for PR.

v6.1.0
======

- Rebuild wheels with qpdf 11.1.1. No new functionality.

v6.0.2
======

- Fixed large increase in binary wheel file size for manylinux wheels.
- Provide macOS and Linux wheels for Python 3.11.

v6.0.1
======

- Use qpdf 11.1.0, which fixes problems with building pikepdf on Windows.

v6.0.0
======

- pikepdf 6.0.0 was released to align with backward incompatible changes in qpdf 11.
- Remove deprecated APIs. Mostly these were public APIs that had no business being
  public.
    - Several functions in pikepdf.jbig2
    - Some helper functions in pikepdf.models.image
    - The property PdfImage.is_inline. (Use isinstance PdfInlineImage instead.)
    - Attempting to copy pages using the ``.copy_foreign`` method now raises an
      exception. Use The ``Pdf.pages`` interface to copy pages.

