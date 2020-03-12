# Doorbel-camera

we want to detect people we’ve never seen before, so we
won’t start with a list of known faces to check against. But even if we don’t
know who someone is, we can still use face recognition to identify them as
the same person each time they come back.
Here’s how we can track people we’ve never seen before using face encodings:
1. Each time we see a face, calculate a face encoding for it using our
face recognition model.
2. Check all the faces we’ve seen previously to see if any of their face
encodings seem to be a near match for this new face.
3. If the new face matches a face encoding we have seen before, we
know we are looking at the same person again! So we can update
the number of times that unnamed person has visited.
4. If the new face encoding doesn’t match any previously seen faces,
create a new record for it in our list of previously seen faces with a
visit count of 1.
As we see more and more faces, the list of seen faces will grow. Eventually
we’ll have a database of everyone who has ever come to our door even
though we won’t know their names.
