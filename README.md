# OCRopus OCR Engine(s)

OCRopus is a collection of neural-network based OCR engines originally developed by Thomas Breuel, with many contributions from students, companies, and researchers. The github.com/ocropus organization collects many of the repositories.

OCRopus has gone through many incarnations:

- hwrec -- a C-based handwriting recognition engine
  - deployed by the US Census Bureau in 1995
  - uses a novel dynamic programming based segmentation algorithm (a decade later used as "seam carving" in computer graphics)
  - neural network character classification
  - recognition lattices
  - decoding using finite state transducers
- OCRopus 1 -- a C++ based OCR engine based on a port of hwrec
  - efficient branch-and-bound geometric layout analysis algorithms
- OCRopus 2 (ocropy) -- a Python port of OCRopus 1
  - this is the most widely used version of OCRopus right now and has several derivative systems
  - robust text line normalization prior to recognition
  - LSTM-based recognizer
- OCRopus 3 -- a PyTorch 0.3 port of OCRopus 2
  - incompatible with later versions of PyTorch, so don't use
  - released as a collection of separate small projects
  - GPU-based recognition
  - trainable page skew and rotation detection
  - trainable layout analysis
  - character-based language models
- OCRopus 4 -- a PyTorch 1.x port of OCRopus 3
  - to be released in 2020
  - deeper models for page segmentation and text recognition
  - word or line-based recognition
  - fully grayscale recognition
  - eliminates the need for text line normalization
  - self-supervised training
  - WebDataset-based I/O
