# v00-06


# v00-05

Marko Petric 2017-04-07 
  - Coverity integration

Marko Petric 2017-04-03 
  - Coverity needs a email address for the upload, add one to upload curl
  - Add coverity scan integration

Marko Petric 2017-03-23 
  - Add install statement to CI
  - Add CONTRIBUTING.md and PULL_REQUEST_TEMPLATE and fix test script

Marko Petric 2017-03-21 
  - Update README

Frank Gaede 2017-03-02 
  - force exception if no cellId encoding in collection
  - fix -Wshadow in DDCaloDigi.cc (namespace dd4hep)
  - fix deprecated localToWorld() in DDCaloHitCreator.cc

Matthias 2017-02-27 
  - simplify code for deltat definition
  - remove warning in DDCaloDigi
  - resolve shadowed declarations
  - fix call of tracker ENDCAP subdetector

Andre Sailer 2017-02-17 
  - Fix indentation flagged by warning
  - Fix warning about sign comparison
  - Remove unnecessary parts for cxx11 flag from CMakeLists, part auf default flags
  - Remove cxx flags, they are not necesseary or part of the defaults
  - Fix warnings: initialise members
  - Create README.md
  - Create LICENSE
  - Enable diagnostic color
  - Add travis config

Andre Sailer 2017-02-08 
  - DDCaloHitCreator: Only create DD4hep::VolumeManager if it does not exist

Frank Gaede 2016-11-23 
  -  updated release notes

Andre Sailer 2016-11-21 
  - DDMarlinPandora:DDCaloHitCreator: add debug output, protect against missing cellIDs
  - DDMarlinPandora::DDTrackCreator add variables to initialiser lists
  - DDMarlinPandora:DDPandoraPfaNewProcessor: fix warnings
  - DDMarlinPandora::DDSimpleMuonDigi: fix two warnings for unused variables
  - DDMarlinPandora:DDGeometryCreator: fix warnings
  - DDMarlinPandora::DDMCParticleCreator fix warnings
  - DDMarlinPandora::DDTrackCreator fix warnings
  - DDMarlinPandora::DDPFOCreator: fix warnings
  - DDMarlinPandora::DDCaloDigi: fix two warnings for unused variables
  - DDMarlinPandora::CaloHitCreator: Fix compiler warnings
  - DDMarlinPandora::CaloHitCreator: get normal vector from detelement instead of using assumptions about calorimeters to calculate phi

Andre Sailer 2016-11-11 
  - DDMarlinPandora: TrackCreatorClic: protect against bad tracks (e.g., without trackstates) in collection

Shaojun Lu 2016-10-14 
  -  Apply the patch from John Marshall to follow the current update in PandoraPFA.

Georgios Voutsinas 2016-07-28 
  - updating to version 00-04

Nikiforos Nikiforou 2016-04-07 
  - Added note to handle exception not caught for very small omega in TrackCreator. Not a problem currently

Nikiforos Nikiforou 2016-04-06 
  - Merged changes in MarlinPandora by Bono up to Mar. 30th
  - Preparing to merge changes from MarlinPandora

Shaojun Lu 2016-03-30 
  -  Apply the Revision 5326 again with the more generic algorithm to calculate 'dt'.

Nikiforos Nikiforou 2016-02-19 
  - Merged changes from ILDCaloDigi, accessing Subdets by det type flags

Frank Gaede 2016-02-19 
  -  - fix: use idDecoder(hit)["module"] ( was 0 )    -> all calo cellID encodings should have module       otherwise this digitizer won't work

Frank Gaede 2016-02-18 
  -  - updated version to ----- v00-03 -----

Nikiforos Nikiforou 2016-02-18 
  - Merging changes in MalrinPandora

Frank Gaede 2016-02-15 
  -  - updated version to  ------------ v00-02 -----  - updated release notes

Frank Gaede 2016-02-14 
  -  - enforce unique selection in getExtension(include,exclude)    - throws exception if not unique  - bug fix: eCalBarrelExtension -> eCalEndcapExtension    for setting m_eCalEndCapInnerZ  - added DetType::FORWARD to excludeFlags for main calorimeters  - added DetType::AUXILIARY to excludeFlag for LCal ( exclude BeamCal )

Nikiforos Nikiforou 2016-02-12 
  - Changes in way of accessing coil info

Frank Gaede 2016-02-12 
  -  - fixed crash in debug printout (*iter -> detElement )  - added debug printout for track selection

Nikiforos Nikiforou 2016-02-11 
  - Major overhaul droppping detector name params
  - Removed tracker/vertex names as parameters

Nikiforos Nikiforou 2016-02-10 
  - Modified DDTrackCreatorCLIC to use detector type flags to access trackers rather than names from processor parameters

Nikiforos Nikiforou 2016-02-08 
  - Changing track selection criteria

Nikiforos Nikiforou 2016-02-04 
  - Changed method of getting subdetector hits, revising track cuts

Nikiforos Nikiforou 2016-01-18 
  - Added units to endcap disk geometry parsing

Shaojun Lu 2016-01-08 
  -  Improve the algorithm to calculate 'dt', and remove the dependence on the barrel stave symmetry, phi position and staveID number. 'float dt = sqrt(dx*dx + dy*dy)' is more generic for any symmetry and phi postion of barrel stave.

Frank Gaede 2015-12-17 
  -  - added dd4hep units to parameters extracted from DD4hep !!

Nikiforos Nikiforou 2015-12-02 
  - Adding missing files
  - Adding missing file

Nikiforos Nikiforou 2015-12-01 
  - Minor changes to ifdef for class renaming
  - Changed all classes to use DDXXXX convention for their names (bonus: avoid clashes with MarlinPandora)

Nikiforos Nikiforou 2015-11-20 
  - Minor changes in DDTrackCreatorCLIC. Cannot proceed before agreeing on conventions for hit counts associated with tracks

Frank Gaede 2015-10-22 
  -   - protect against poor tracks ( ndf <0 or missing/poor parameters)     ( eventuall needs to be done in the tracking code ...)

Frank Gaede 2015-10-05 
  -  - changed formatting

Nikiforos Nikiforou 2015-09-29 
  - Minor fix in absorber correction to recover the same MIP-equivalent energy in CaloHits as MarlinPandora

Frank Gaede 2015-09-08 
  -  - call DDTrackCreatorILD if requested ...

Nikiforos Nikiforou 2015-09-07 
  - Adding DDTrackCreatorBase and separate implementations for ILD and CLIC

Nikiforos Nikiforou 2015-08-27 
  - Removed final dependence on Gear within DDTrackCreator.cc
  - Fixed bug in DDCaloHitCreator.cc

Nikiforos Nikiforou 2015-08-19 
  - Various fixes to be made compatible with new DDRec structure
  - Removed unnecessary variables, moved to new DDRec structure

Nikiforos Nikiforou 2015-08-18 
  - Made more streamlined, removed extra parameters from setting structures

Frank Gaede 2015-07-31 
  -  - added some debug put ut for failed tracks

Frank Gaede 2015-07-17 
  -  - minimal release notes
  -  - added some debug printout

Nikiforos Nikiforou 2015-07-15 
  - Enabled access to different solenoid name

Frank Gaede 2015-07-15 
  -  - fixed build flags for MacOs and clang
  - Fixed missing parameter name

Nikiforos Nikiforou 2015-07-14 
  - More updates

Nikiforos Nikiforou 2015-07-10 
  - Moved TrackCreator to DDTrackCreator
  - Moved extra const parameters from main classs to respective Settings classes. Also introduced detector names as processor parameters and settings members

Nikiforos Nikiforou 2015-07-07 
  - Commit forgotten DDSimpleMuonDigi

Nikiforos Nikiforou 2015-06-29 
  - Adding a Calo Digitizer based on DD4hep
  - Initial import of source files from MarlinPandora modified with DD4hep integration

Frank Gaede 2015-06-29 
  -   empty package structure