# FlareObjects_in_MeerKAT_LSPs
This repository has code for combining public catalogues of flare type objects into a single catalogue, as well as combining to coordinates of MeerKAT large survey project (LSP) pointings into one cataloue. It then has code to compare the two catalogues to find flare type object that fall into the field of view of MeerKAT LSPs.

The flare type object catalogues we use are:
<ul>
  <li><a href="https://ui.adsabs.harvard.edu/abs/2011AJ....142..138L/abstract">Lepine</a>: bright M-dwarfs</li>
  <li><a href="https://jgagneastro.com/list-of-ultracool-dwarfs/">JGagne</a>: ultra-cool dwarfs</li>
  <li><a href="https://ui.adsabs.harvard.edu/abs/2013MNRAS.429.2934K/abstract">sdss_mwds</a>: magnetic white dwarfs from SDSS</li>
  <li><a href="https://ui.adsabs.harvard.edu/abs/2009ApJ...696..870D/abstract">Catalina</a>: Transients in the Catalina Surveys Data Release 2</li>
  <li>simbad_fstars: flare stars (F*) from the SIMBAD catalogue (2000A&AS..143....9W)</li>
  <li>simbad_RSCVns: flare stars (RS*) from the SIMBAD catalogue (2000A&AS..143....9W)</li>
  <li><a href="http://www.montrealwhitedwarfdatabase.org/references.html">White dwarfst</a>: white dwarfs from the Montreal White Dwarf Database</li>
</ul>

The MeerKAT LSPs we consider are:
<ul>
  <li>MIGHTEE</li>
  <li>MALS</li>
  <li>MHONGOOSE</li>
  <li>LADUMA</li>
  <li>Fornax</li>
  <li>ThunderKAT</li>
</ul>
The pointing information for some of these is proprietary information, so has not been included here.

The included jupyter notebooks perform the following functions:
<ul>
  <li>Collate_FlareObjectCatalogues.ipynb - combine the flare object catalogues into one catalogue for matching</li>
  <li>ReorganiseLSP_Information.ipynb - get the pointing information for each LSP and combine into one catalogue</li>
  <li>MatchFlareStar_LSPs.ipynb - match the flare object and LSP catalogues to find which flare objects are in the field of view of LSP pointings</li>
  <li>FlareObjects_In_LSP_FoVs.ipynb - all three of the above scripts combined into one handy-dandy script</li>
</ul>

All of these scripts require pandas, astropy, and astroquery.
