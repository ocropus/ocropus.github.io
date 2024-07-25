# OCRopus OCR Engine(s)

OCRopus is a collection of neural-network based OCR engines originally developed by Thomas Breuel, with many contributions from students, companies, and researchers. The github.com/ocropus organization collects many of the repositories.

OCRopus has gone through many incarnations:

- **hwrec** -- a C-based handwriting recognition engine
  - deployed by the US Census Bureau in 1995
  - uses a novel dynamic programming based segmentation algorithm (a decade later used as "seam carving" in computer graphics)
  - neural network character classification
  - recognition lattices
  - decoding using finite state transducers
- **OCRopus 1** -- a C++ based OCR engine based on a port of hwrec
  - efficient branch-and-bound geometric layout analysis algorithms
- **[OCRopus 2 = ocropy](https://github.com/ocropus/ocropy)** -- a Python port of OCRopus 1
  - this is the most widely used version of OCRopus right now and has several derivative systems
  - robust text line normalization prior to recognition
  - LSTM-based recognizer
- **OCRopus 3** -- a PyTorch 0.3 port of OCRopus 2
  - incompatible with later versions of PyTorch, so don't use
  - released as a collection of separate small projects
  - GPU-based recognition
  - trainable page skew and rotation detection
  - trainable layout analysis
  - character-based language models
- **OCRopus 4** -- a PyTorch port of OCRopus 3 with many new features
  - deeper models for page segmentation and text recognition
  - word or line-based recognition
  - direct segmentation and recognition on grayscale images
  - eliminates the need for text line normalization
  - self-supervised training
  - WebDataset-based I/O
 
# Consulting / Support

For commercial consulting or support, please contact **consulting@ocropus.org**
  
# Related Projects

- **[Calamari OCR](http://github.com/Calamari-OCR/calamari)** --  Text line recognizer based on OCRopy and Kraken
- **[Kraken OCR](https://github.com/mittagessen/kraken)** --  Turnkey OCR system optimized for historical and non-Latin script materials derived from OCRopy.
- **[Tesseract OCR](https://github.com/tesseract-ocr)** -- OCR system that contains a heavily modified C++ port of ocropy's line recognizer

# Related Tools

- **[hocr-tools](http://github.com/ocropus/hocr-tools)** -- tools for manipulating the hOCR OCR output format
- **[ocrodeg](http://github.com/ocropus/ocrodeg)** -- automated document degradation of binary images

# Obsolete Tools
  
- **[cctc](https://github.com/ocropus/cctc)**, **[cctc2](https://github.com/ocropus/cctc2)** -- CTC implementations for PyTorch 
  - not needed anymore--use the native bindings)
- **[pyopenfst](https://github.com/ocropus/pyopenfst)**
  - simple bindings of OpenFST to Python (not needed anymore--use the native bindings)
