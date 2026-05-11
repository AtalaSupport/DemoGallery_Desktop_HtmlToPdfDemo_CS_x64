# HTML to PDF Demo
A very simple console app that converts a HTML file into a PDF by using in a memory-efficient way using FileSystemImageSource.  

Who says you always need a viewer in an imaging application?  

This console app uses our FileSystemImageSource to read each frame of the target file directly into a PDF Encoder. Each page read will trigger a Compression Selector event so you can choose the best compression to use for that specific page's Pixel Format.  

This approach can easily be adapted to services or plumbed in to batch-based processing.  

By setting a handler for PdfEnc.SetEncoderCompression, we are able to dynamically select the most appropriate form of image compression to apply, based on the PixelFormat (color depth) of each page.  

