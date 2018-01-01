12/10/2017: *DKJ* 
started london_documents.xml stored in GitHub: 
URL https://github.com/djakacki/REEDLondon/blob/master/london_documents.xml

*Used James Cummings' taxonomy structure for Staffordshire*

Taxonomy structure:
# bibliography_sections
# record_types
# repositories - kept Staffordshire repositories with comment that they are not used for REED London/Inns of Court
# short_title_catalogues

Naming structure (which will be extended to all REED London refs):
# all xml:ids begin with #RL (expample: RLGIPB1 is REED London Gray's Inn Pension Book 1). I believe this is in keeping with the nomenclature used for Staffordshire and other eREED collections.

At this point I think it makes sense to expand the repository listing to include the other London-centric collections, at least for the printed volumes.

Because this file is an approximation of the work presented in the printed version of *Inns of Court* I've created an "Introduction" section before the "Sources" section. I find this contextual information to helpful - in terms of keeping track of Alan H. Nelson's process of using sources.

The Appendices (Vol. 3) also have a list of Sources, and one question we should ask is whether those sources should be folded into the record source section or not. It might make sense to do so with a reference (perhaps in "edDesc"?) to the fact that they come from the Appendix.

12/22/2017 *DKJ*
Each document is structured based on that developed by James Cummings and REED staff for Staffordshire:

Repositories are all given xml:id's (list below)
Within <biblList> each entry follows this pattern:
    <msDesc xml:id="RL___">
        <msIdentifier>
            <settlement>Location of repository</settlement>
                <repository sameAs="#__"/> (where this ID is for the repository)
                <idno type="shelfmark"></idno> (have defaulted to "shelfmark")
                <msName>TITLE OF WORK</msName> 
        </msIdentifier>
        <ab type="edDesc"></ab> (if there is a description or editorial note about the document, it goes here)
        <ab type="techDesc"><date></date></ab> (document description from "The Documents" section goes here)
    </msDesc>

** For Personal correspondence, I have been using the naming structure: RLPC00# - where RL = Reed London, PC = Personal Correspondence, and 00# is a three digit numbering system starting at 001.

** For "Diaries and Reminiscences" I have been using the naming structure:
RLDR00# - same as above, and DR = Diaries Reminiscences

** Where printed contemporary documents are referred to (e.g., Actes and Monuments, Stow's Annals) I have used <ab type="pubDesc"> with the information drawn from the title page as transcribed by Nelson. Where an ESTC or Wing catalog reference is listed, there is no settlement or repository given.

