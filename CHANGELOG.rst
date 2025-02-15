^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package hri_msgs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.5.0 (2022-05-02)
------------------
* add social engagement msg with 5 discrete levels
* add confidence to Expression message
* update README
* Contributors: Séverin Lemaignan

0.4.1 (2022-01-25)
------------------
* CMakeLists: update references to BodyPosture and Gesture messages
* add BSD LICENSE file
* Contributors: Séverin Lemaignan

0.4.0 (2022-01-25)
------------------
* split BodyAttitude into BodyPosture and Gesture
* Contributors: Séverin Lemaignan

0.3.0 (2022-01-21)
------------------

* remove GroupsStamped and GazesStamped
  GroupsStamped and GazesStamped are essentially arrays of Groups and Gazes, they are not needed as
  nodes would simply publish several message on the corresponding topics
* {GazeSenderReceiver->Gaze}.msg and rename fields in Group.msg and GazeSenderReceiver.msg
* add LiveSpeech.msg for encoding of incremental results of speech-to-text
* Contributors: Séverin Lemaignan

0.2.1 (2022-01-12)
------------------
* update CMakeLists following removing/renaming of messages
* Contributors: Séverin Lemaignan

0.2.0 (2022-01-12)
------------------
* AgeAndGender.msg -> SoftBiometrics.msg
* remove RoIStamped, as not necessary
  The original rationale was to be able to match the RoI to the orginal sourc eimage via the timestamp,
  but it was clunky, and we have decided instead to republish the face image under cropped, alleviating
  the need for the connection to the source image.
* IdsMatch: revise semantic to enable eg face<->body matches
* Contributors: Séverin Lemaignan

0.1.2 (2021-12-01)
------------------
* Added IdsMatch.msg to publish potential matches between face/body/voice ids
  and person ids

0.1.1 (2021-11-09)
------------------
* Added CHANGELOG

0.1.0 (2021-11-09)
------------------
* package.xml format 3 + clean up of unused dependencies
* Removed services which do not make sense in the current ros4hri standard
* IdsList.msg: add a header
  This is critical to be able to reliably match the list of tracked faces/bodies/voices to actually face/body/voice subtopics.
* IdsList and RegionOfInterestStamped were not actualyl built
* Added a stamped version of RegionOfInterest
  This is important to associate the timestamp of the original image to eg a detected face RoI
* add msg for list of face/body/voice/person ids
* FacialLandmarks coordinates are in normalised pixels
  This now matches what PointOfInterest2D stores.
* Github links in README
* Added AudioFeatures.msg, based on INTERSPEECH features
* Update AgeAndGender.msg (capitalisation)
* Delete BodyPose.msg
* Typo fixes
* Update README.md
* Fixed typos in Skeleton2D.msg
* Fixed merge artifacts introduced in 08fdcc5b
* Revert "Update Expression.msg": constants *must* by capitalised
  This reverts commit 79162c9499cb94754b77ff4a58ea1d000c2861bd.
* Update Expression.msg
* Merge branch 'master' of https://git.brl.ac.uk/ROS4HRI/hri_msgs
* msgs edits an cmake additions
* Update list of msg in CMakeLists
* Delete Person.msg
* Update BodyLang.msg
* Cmakelists edits
* Delete settings.json
* Delete Faces.msg
* Delete Face.msg
* Delete ActionUnit.msg
* Update ActionUnits.msg
* Delete BodyStamped.msg
* Delete Body.msg
* Delete FaceROIStamped.msg
* Delete FaceStamped.msg
* Delete Face.msg
* Delete Faces.msg
* Add new file
* Add new file
* Add new file
* Delete Group.msg
* Delete PersonsStamped.msg
* Delete ReidentificationStamped.msg
* Delete Reidentification.msg
* msgs edits
* edits
* Update PersonsStamped.msg
* Update Person.msg
* Add new file
* Add new file
* Delete HeadPoseStamped.msg
* Delete HeadPose.msg
* Update GazeSenderReceiver.msg
* Delete FacesLandmarks.msg
* Update Faces.msg
* Update AgeGender.msg
* Add new file
* Delete FacesActionUnits.msg
* Update FacialLandmarksStamped.msg
* Delete AgeGenderStamped.msg
* Delete EmotionsStamped.msg
* Update Emotion.msg
* Update Emotion.msg
* Created a Face.msg describing the face model
* emotions, headpose, age and gender msgs added.
* social_net msgs file added to be refractored
* skeleton_msgs edit
* skeleton edits
* skeleton points added
* Fixed travis.yml for ROS1
* Fixed messages names
* Slightly simply travis.yml
* WIP travis
* travis WIP
* travis WIP
* travis WIP
* travis WIP
* travis WIP
* Added travis badge to readme
* First attempt at travis integration
* Added Person.location_known_confidence with doc
* Clarify the semantics of UpdateHuman.srv
* Reworked the face + face landmarks msgs
* Added services to communicate with the humans_server database
* Added Group.msg
* Added msg associating faces to their AUs + updated CMakeLists
* Added a message for action units
* Added Person.msg
* Update link to wiki
* {PixelCoordinate->PointOfInterest2D} + added a confidence level
* gitlab doesn't like backticks in links
* Added a FacialLandmarks msg
* Making sure the package compiles successfully
* Added README
* first commit
* Contributors: Séverin Lemaignan, Youssef Mohamed, yef2-mohamed
