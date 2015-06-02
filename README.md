# BAMSpector
A lightweight shiny application to visualize gene models and supporting reads.

The goal is to produce a shiny application that allows the user to
specify a gene symbol and BAM file(s), and be rewarded with a
visualization displaying the gene model (exons organized into
transcripts) and supporting reads. The application should use the
release version of Bioconductor.

For gene models, the server might consult org.Hs.eg.db to map from
gene symbol to Entrez gene id, then extract the gene model from the
appropriate TxDb.Hsapiens.* (these steps might be combined using
Homo.sapiens).

For coverage, Rsamtools might be handy, using the range() of the gene
model.

For display, the server might use Gviz to visualize the gene model,
and to add coverage track(s).

The resulting application should be easy enough to understand.  An
only moderately experienced Bioconductor user should feel like they
themselves could build the app from scratch.
