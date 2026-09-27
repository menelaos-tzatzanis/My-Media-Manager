# MyMediaManager

**Local-first desktop εφαρμογή για Windows για οργάνωση φωτογραφιών, βίντεο και audio σε μία ενιαία δομημένη βιβλιοθήκη.**

[English](README.md) · [Ελληνικά](README_GR.md)

---

## Παρουσίαση

Το MyMediaManager είναι μια desktop εφαρμογή για Windows, σχεδιασμένη ώστε να συγκεντρώνει φωτογραφίες, βίντεο και audio σε μία οργανωμένη τοπική βιβλιοθήκη πολυμέσων.

Αντί να βασίζεται μόνο σε φακέλους, η εφαρμογή προσθέτει πιο ευέλικτη οργάνωση μέσω albums, nested albums, tags, favorites, profiles προσώπων, υποβοηθούμενης offline αναγνώρισης προσώπων, προηγμένης αναζήτησης, playlists και άλλων εργαλείων διαχείρισης της βιβλιοθήκης.

Το media μπορεί να εισάγεται από υπάρχοντες φακέλους, να μεταφέρεται απευθείας από κινητό μέσω του τοπικού δικτύου, να οργανώνεται κατά την εισαγωγή, να επεξεργάζεται όταν διαχειρίζεται από την εφαρμογή και να εξάγεται ξανά όταν απαιτείται.

Η εφαρμογή υποστηρίζει δύο βασικούς τρόπους διαχείρισης αρχείων:

- **Linked media**, που παραμένει στην αρχική του τοποθεσία
- **Managed media**, που αποθηκεύεται μέσα στη δική της τοπική βιβλιοθήκη

Στόχος είναι μια μεγάλη προσωπική συλλογή πολυμέσων να γίνεται ευκολότερη στην οργάνωση, την αναζήτηση και τη χρήση, χωρίς να απαιτείται υποχρεωτική cloud-based βιβλιοθήκη.

> **Portfolio showcase:** Αυτό το δημόσιο repository παρουσιάζει την εφαρμογή και το interface της. Ο production πηγαίος κώδικας διατηρείται ιδιωτικός και δεν δημοσιεύεται εδώ.

![MyMediaManager - Media Library](assets/screenshots/01-all-media.png)

---

## People & Faces

Το MyMediaManager περιλαμβάνει τοπικά εργαλεία για την οργάνωση φωτογραφιών γύρω από τα πρόσωπα που εμφανίζονται σε αυτές.

Ο χρήστης μπορεί να δημιουργεί profiles προσώπων και να συνδέει κάθε profile με ένα κανονικό tag της βιβλιοθήκης.

Κάθε profile μπορεί να περιέχει πολλαπλά reference faces από διαφορετικές φωτογραφίες, γωνίες και συνθήκες.

Έτσι, το People workflow γίνεται μέρος του κανονικού συστήματος tagging και όχι μια απομονωμένη λειτουργία.

![MyMediaManager - People and Faces](assets/screenshots/03-people-faces.png)

---

## Υποβοηθούμενη Offline Αναγνώριση Προσώπων

Όταν ένα profile έχει αρκετά χρήσιμα reference faces, το MyMediaManager μπορεί να αναζητήσει στη τοπική βιβλιοθήκη πιθανές αντιστοιχίσεις.

Οι προτάσεις εμφανίζονται για έλεγχο και δεν αντιμετωπίζονται αυτόματα ως σωστές.

Ο χρήστης μπορεί να:

- Ελέγξει προτεινόμενα πρόσωπα
- Δει High Confidence και Possible matches
- Επιβεβαιώσει μια αντιστοίχιση
- Απορρίψει μια αντιστοίχιση
- Αγνοήσει μόνιμα μια λανθασμένη πρόταση
- Επιλέξει recognition references
- Αναζητήσει σε ολόκληρη τη βιβλιοθήκη ή σε επιλεγμένα albums

Όταν μια αντιστοίχιση επιβεβαιωθεί, το συνδεδεμένο tag του προσώπου μπορεί να εφαρμοστεί στη σχετική φωτογραφία.

Αυτό μπορεί να επιταχύνει σημαντικά τη δημιουργία χρήσιμων person-based tags σε μεγαλύτερες συλλογές φωτογραφιών.

![MyMediaManager - Face Recognition Review](assets/screenshots/04-face-recognition.png)

Η αναγνώριση προσώπων είναι **εργαλείο υποβοήθησης της οργάνωσης** και όχι εγγύηση τέλειας αναγνώρισης.

Μπορεί να προτείνει λανθασμένη αντιστοίχιση ή να μην εντοπίσει κάποιο πρόσωπο, γι' αυτό η τελική επιβεβαίωση παραμένει πάντα στον χρήστη.

Η αναγνώριση γίνεται απέναντι στα profiles που έχουν δημιουργηθεί μέσα στη δική του τοπική βιβλιοθήκη και δεν αποτελεί Internet identity-search service.

---

## Daphne — Προηγμένη Αναζήτηση Βιβλιοθήκης

Η Daphne είναι ο βοηθός αναζήτησης της βιβλιοθήκης του MyMediaManager.

Παρέχει έναν πιο πρακτικό τρόπο να συνδυάζονται πολλά κριτήρια αναζήτησης χωρίς ο χρήστης να χρειάζεται να περιηγείται χειροκίνητα σε albums και tags ένα-ένα.

Τα κριτήρια μπορούν να περιλαμβάνουν συνδυασμούς όπως:

- Tags
- Albums
- Excluded tags
- Excluded albums
- Match all conditions
- Match at least one condition
- Media type
- Library state
- File size
- Date-related criteria
- Saved searches

Για παράδειγμα, ο χρήστης μπορεί να αναζητήσει:

**Helen + Sofia, αλλά όχι Alex**

και να πάρει αμέσως τα media που ταιριάζουν.

Τα αποτελέσματα μπορούν στη συνέχεια να επιλεγούν και να εξαχθούν απευθείας.

![MyMediaManager - Daphne Search](assets/screenshots/07-daphne-search.png)

Η Daphne λειτουργεί πάνω στις πληροφορίες που έχουν ήδη αποθηκευτεί στη τοπική βιβλιοθήκη και είναι σχεδιασμένη ως focused media-search και organization assistant, όχι ως γενικού σκοπού cloud chatbot.

---

## Phone Import

Το MyMediaManager μπορεί να λαμβάνει φωτογραφίες, βίντεο και υποστηριζόμενο audio απευθείας από κινητό μέσω του τοπικού δικτύου.

Η desktop εφαρμογή ξεκινά ένα προσωρινό Phone Import session και παρέχει QR code, το οποίο μπορεί να ανοιχτεί από κινητό που βρίσκεται στο ίδιο trusted Wi-Fi network.

Το mobile upload workflow μπορεί να χρησιμοποιηθεί για:

- Επιλογή αρχείων από το κινητό
- Άμεσο upload στη desktop library
- Επιλογή υπάρχοντος album
- Δημιουργία νέου album πριν από το upload
- Εφαρμογή υπαρχόντων tags
- Δημιουργία νέων tags
- Οργάνωση των media πριν φτάσουν στην κύρια βιβλιοθήκη

Έτσι, για παράδειγμα, ένα σύνολο φωτογραφιών διακοπών μπορεί να φτάσει ήδη μέσα στο σωστό album, αντί να απαιτεί πλήρη οργάνωση αργότερα.

![MyMediaManager - Phone Import](assets/screenshots/11-phone-import.png)

Το Phone Import λειτουργεί μέσω του τοπικού δικτύου και browser-based upload page.

Δεν παρουσιάζεται ως ξεχωριστή native mobile εφαρμογή ή cloud-storage service.

Ευαίσθητες πληροφορίες τοπικής σύνδεσης έχουν αφαιρεθεί από το δημόσιο portfolio screenshot.

---

## Albums, Nested Albums & Υπάρχουσες Δομές Φακέλων

Τα albums αποτελούν ένα ευέλικτο επίπεδο οργάνωσης πάνω από τα πραγματικά media files.

Το MyMediaManager υποστηρίζει:

- Albums
- Nested albums
- Το ίδιο media σε πολλαπλά albums
- Album search
- Προσθήκη και αφαίρεση media από albums
- Import φακέλων απευθείας ως albums

Μια υπάρχουσα δομή φακέλων μπορεί να επαναχρησιμοποιηθεί αντί να ξαναφτιαχτεί χειροκίνητα.

Για παράδειγμα:

```text
Vacations 2026
├── Summer
└── Winter
```

μπορεί να γίνει αντίστοιχη δομή albums μέσα στο MyMediaManager.

Τα ονόματα φακέλων και υποφακέλων μπορούν έτσι να μετατραπούν σε χρήσιμα album names κατά την εισαγωγή.

Το ίδιο media item μπορεί επίσης να ανήκει σε περισσότερα από ένα albums χωρίς να απαιτείται ξεχωριστό φυσικό αντίγραφο για κάθε album relation.

---

## Tags, Favorites & Ευέλικτη Οργάνωση

Τα albums είναι μόνο ένας από τους τρόπους οργάνωσης της βιβλιοθήκης.

Τα tags προσθέτουν ένα ακόμα ανεξάρτητο επίπεδο που μπορεί να χρησιμοποιείται σε διαφορετικά albums και media types.

Τα tags μπορούν να αντιπροσωπεύουν, για παράδειγμα:

- Πρόσωπα
- Τοποθεσίες
- Events
- Themes
- Categories
- Προσωπικά labels οργάνωσης

Τα media μπορούν επίσης να σημειώνονται ως Favorites για γρήγορη πρόσβαση.

Ο συνδυασμός albums, tags, people profiles και favorites επιτρέπει στην ίδια συλλογή να οργανώνεται με περισσότερους από έναν χρήσιμους τρόπους, χωρίς να χρειάζεται κάθε φορά να αλλάζει η αρχική δομή φακέλων.

---

## Photo Viewer

Ο ενσωματωμένος media viewer κρατά το επιλεγμένο photo μαζί με τις βασικές πληροφορίες και ενέργειες της βιβλιοθήκης.

Ανάλογα με το επιλεγμένο media και το storage mode, ο viewer μπορεί να παρέχει:

- Full-size viewing
- Previous / next navigation
- Zoom
- Rotation
- Flip
- Full screen
- Favorite status
- File information
- Image dimensions
- File size
- Albums
- Tags
- Date tools
- Rename
- Copy
- Managed-photo tools

![MyMediaManager - Photo Viewer](assets/screenshots/05-photo-viewer.png)

---

## Επεξεργασία Managed Photos

Τα Managed photos μπορούν να επεξεργάζονται απευθείας μέσα από την εφαρμογή.

Τα διαθέσιμα photo tools περιλαμβάνουν:

- Black & white
- Auto enhance
- Auto contrast
- Image adjustments
- Saturation
- Sharpness
- Straighten
- Border / margin
- Crop
- Rotate
- Flip

![MyMediaManager - Photo Editing](assets/screenshots/08-photo-editing.png)

Η ακριβής συμπεριφορά εξαρτάται από το επιλεγμένο editing operation.

Η εφαρμογή δεν παρουσιάζει όλες τις επεξεργασίες ως αυτόματα non-destructive.

---

## Optimized Copies

Το MyMediaManager μπορεί να δημιουργεί ξεχωριστό optimized JPEG copy από ένα Managed image.

Έτσι ο χρήστης μπορεί να διατηρεί το αρχικό library item και ταυτόχρονα να δημιουργεί μια μικρότερη έκδοση για περιπτώσεις όπου το file size έχει σημασία.

Οι album και tag relationships μπορούν επίσης να μεταφέρονται στο νέο optimized copy.

Στο παρακάτω πραγματικό παράδειγμα από τη demo library, ένα **PNG 2.4 MB** δημιούργησε ένα optimized **JPEG 444 KB**.

![MyMediaManager - Optimized Copy](assets/screenshots/09-optimize-copy.png)

Αυτό αποτελεί ένα συγκεκριμένο παράδειγμα από τη βιβλιοθήκη επίδειξης.

Η πραγματική μείωση μεγέθους εξαρτάται από το αρχικό image και τις επιλεγμένες processing settings.

---

## Slideshow

Το ενσωματωμένο slideshow μπορεί να παρουσιάζει library media σε focused full-screen προβολή.

Οι διαθέσιμες επιλογές περιλαμβάνουν:

- Ρυθμιζόμενο slide interval
- Current-order playback
- Alternative ordering
- Repeat from beginning
- Manual previous / next navigation
- Full-screen presentation

![MyMediaManager - Slideshow](assets/screenshots/10-slideshow.png)

Η αναπαραγωγή audio από τον player της εφαρμογής μπορεί να συνεχίζεται όσο προβάλλονται φωτογραφίες, επιτρέποντας slideshow με μουσική.

Η αναπαραγωγή video αντιμετωπίζεται ξεχωριστά ώστε να αποφεύγεται ανταγωνιστικό audio playback όπου χρειάζεται.

---

## Audio & Playlists

Το MyMediaManager δεν περιορίζεται στις φωτογραφίες.

Τα audio files μπορούν επίσης να οργανώνονται και να αναπαράγονται μέσα στην ίδια βιβλιοθήκη.

Η λειτουργία playlists περιλαμβάνει:

- Δημιουργία playlists
- Προσθήκη audio tracks
- Reordering playlist items
- Αναπαραγωγή μεμονωμένου track
- Play from start
- Previous / next controls
- Διαφορετικά playback modes
- Export playlist content

![MyMediaManager - Audio Playlist](assets/screenshots/06-audio-playlists.png)

Έτσι, photos, videos και audio μπορούν να παραμένουν μέρος της ίδιας ευρύτερης προσωπικής media library χωρίς να απαιτούν εντελώς ξεχωριστό σύστημα οργάνωσης.

---

## Linked & Managed Media

Το MyMediaManager υποστηρίζει δύο διαφορετικές προσεγγίσεις για τα τοπικά αρχεία.

### Linked Media

Τα Linked media παραμένουν στην υπάρχουσα τοποθεσία τους στον υπολογιστή ή σε συνδεδεμένο storage.

Η εφαρμογή αποθηκεύει τη σχετική library σχέση χωρίς να χρειάζεται να δημιουργήσει νέο Managed copy του αρχικού αρχείου.

Αυτό είναι χρήσιμο για χρήστες που έχουν ήδη οργανωμένη δομή φακέλων ή μεγάλη υπάρχουσα media collection.

Αν ένα Linked file μετακινηθεί ή πάψει να είναι διαθέσιμο, το MyMediaManager περιλαμβάνει missing-media detection και relinking εργαλεία.

### Managed Media

Τα Managed media αντιγράφονται στο δικό του τοπικό library storage.

Έτσι το MyMediaManager αποκτά άμεσο έλεγχο πάνω στο αποθηκευμένο copy και μπορεί να υποστηρίζει workflows όπως:

- Managed-photo editing
- Optimized copies
- Managed backup
- Library-controlled storage

Linked και Managed items μπορούν να συνυπάρχουν μέσα στην ίδια library.

---

## Import Media

Τα media μπορούν να εισέρχονται στη βιβλιοθήκη μέσα από διαφορετικά workflows.

Περιλαμβάνονται:

- Προσθήκη μεμονωμένων φακέλων
- Import folder as album
- Import nested folder structures
- Phone Import
- Managed import
- Linked import

Όπου είναι κατάλληλο, η υπάρχουσα οργάνωση μπορεί να διατηρείται αντί να ξαναφτιάχνεται από την αρχή.

---

## Export & Sharing

Η οργάνωση media μέσα στο MyMediaManager δεν σημαίνει ότι τα αρχεία εγκλωβίζονται μέσα στην εφαρμογή.

Ανάλογα με το workflow, ο χρήστης μπορεί να εξάγει:

- Selected media
- Search results
- Album-related selections
- Person-profile photos
- Playlist content
- Files σε κανονικούς φακέλους
- ZIP packages

Υποστηρίζεται επίσης Windows sharing σε σχετικά workflows.

Έτσι η βιβλιοθήκη μπορεί να χρησιμοποιείται τόσο για μακροχρόνια οργάνωση όσο και για γρήγορη δημιουργία ενός συγκεκριμένου set αρχείων για χρήση αλλού.

---

## Backup & Restore

Το MyMediaManager περιλαμβάνει τοπικά εργαλεία Backup και Restore.

Ένα library backup μπορεί να περιλαμβάνει:

- Database snapshot
- Managed media
- Thumbnails
- Backup metadata / manifest

Οι restore λειτουργίες περιλαμβάνουν validation και confirmation πριν αντικατασταθεί η ενεργή βιβλιοθήκη.

Επειδή τα **Linked media** παραμένουν έξω από το Managed storage της εφαρμογής, τα αρχικά εξωτερικά Linked files δεν αντιγράφονται αυτόματα μέσα σε ένα MyMediaManager backup.

Ο χρήστης παραμένει υπεύθυνος για ξεχωριστό backup αυτών των αρχικών εξωτερικών αρχείων.

---

## Dashboard & Library Health

Το Dashboard παρέχει συνολική εικόνα της τρέχουσας βιβλιοθήκης μαζί με πληροφορίες maintenance και storage.

Μπορεί να εμφανίζει πληροφορίες όπως:

- Total media
- Linked media
- Managed media
- Videos
- Audio
- Favorites
- Missing media
- Untagged media
- Unsorted media
- Duplicate information
- Database size
- Thumbnail storage
- Managed-file storage
- Total local library storage

Τα maintenance tools περιλαμβάνουν:

- Library Health
- Check Missing
- Relink Folder
- Scan EXIF Dates
- Clean orphaned thumbnails
- Library information
- Library statistics

![MyMediaManager - Dashboard](assets/screenshots/02-dashboard.png)

Αυτά τα εργαλεία βοηθούν τον χρήστη να κατανοεί και να συντηρεί την κατάσταση μιας μεγαλύτερης τοπικής media collection, αντί η βιβλιοθήκη να λειτουργεί σαν ένα κλειστό “black box”.

---

## Local-First Σχεδιασμός

Το MyMediaManager είναι σχεδιασμένο γύρω από local media ownership και local processing.

Η βασική λειτουργία της εφαρμογής δεν απαιτεί:

- Υποχρεωτικό cloud account
- Remote media database
- Remote face-recognition service
- Browser-based hosting
- Συνεχή σύνδεση στο Internet

Οι κανονικές πληροφορίες της βιβλιοθήκης αποθηκεύονται τοπικά στον Windows υπολογιστή.

Το face detection και το face matching πραγματοποιούνται τοπικά με τα recognition components της εφαρμογής.

Το Phone Import μεταφέρει επίσης media μέσω του τοπικού δικτύου και δεν απαιτεί cloud media account.

Ορισμένες ρητά επιλεγμένες sharing actions μπορεί να ανοίγουν ή να χρησιμοποιούν εξωτερικές υπηρεσίες, αλλά αυτές είναι ξεχωριστές από την κανονική λειτουργία της βιβλιοθήκης.

---

## Απόδοση & Μεγάλες Βιβλιοθήκες

Η εφαρμογή περιλαμβάνει τεχνικές υλοποίησης που έχουν στόχο να παραμένει πρακτική και με μεγαλύτερες libraries.

Περιλαμβάνονται μηχανισμοί όπως:

- Bounded database queries
- Paging
- Virtualized media views
- On-demand operations
- Controlled background work
- Thumbnail caching
- Bounded recognition processing

Το development και το regression testing καλύπτουν επίσης σενάρια με μεγαλύτερες media collections και long-running library operations.

Στόχος είναι το browsing και η οργάνωση να παραμένουν πρακτικά όσο μεγαλώνει η βιβλιοθήκη, χωρίς να χρειάζεται συνεχής επεξεργασία ολόκληρου του library.

---

## Ασφάλεια Δεδομένων & Αξιοπιστία

Διάφορα σημεία της εφαρμογής έχουν σχεδιαστεί ειδικά για πιο ασφαλή διαχείριση τοπικών media libraries.

Παραδείγματα:

- Missing-media detection
- Relinking Linked files
- Managed / Linked separation
- Backup validation
- Restore validation
- Thumbnail cleanup
- Import validation
- Recovery-related handling
- Guarded bulk operations

Η ανάπτυξη περιλαμβάνει regression testing για imports, exports, backup, restore, bulk operations, People / Faces, recognition workflows και μεγαλύτερες libraries.

---

## Τεχνολογία

Το MyMediaManager χρησιμοποιεί τεχνολογίες όπως:

- **Tauri 2**
- **React**
- **TypeScript**
- **Rust**
- **SQLite**
- Local face-recognition components
- Local image-processing tools
- Local media-processing tools
- Windows desktop packaging με NSIS

Το Rust backend χειρίζεται περιοχές όπως:

- Database operations
- Local file management
- Imports
- Exports
- Backup και Restore
- Media processing
- Phone Import services
- Native desktop functionality

Το interface υλοποιείται με React και TypeScript μέσα στο Tauri desktop environment.

---

## Φιλοσοφία Προϊόντος

Το MyMediaManager βασίζεται σε μια απλή ιδέα:

**μια προσωπική media collection πρέπει να παραμένει εύκολη στην οργάνωση, την αναζήτηση, την προβολή και την εξαγωγή χωρίς ο χρήστης να είναι υποχρεωμένος να παραδώσει τον έλεγχο της βιβλιοθήκης του σε ένα υποχρεωτικό cloud platform.**

Η εφαρμογή συνδέει αρκετά καθημερινά workflows:

**import → organize → recognize → find → view → edit → export**

διατηρώντας τη βιβλιοθήκη τοπικά.

Πρόκειται για έναν ευρύτερο personal media organizer και όχι απλώς για photo viewer, με photos, videos και audio μέσα στην ίδια εφαρμογή.

---

## Demo & Privacy Note

Το κύριο photo-demo υλικό και τα person profiles που εμφανίζονται σε αυτό το repository δημιουργήθηκαν ειδικά για την portfolio παρουσίαση και χρησιμοποιούν φανταστικά πρόσωπα και δεδομένα επίδειξης.

Τα ονόματα **Helen**, **John**, **Sofia** και **Alex** είναι demo profile names.

Οι τίτλοι audio που εμφανίζονται στο δημόσιο playlist screenshot τροποποιήθηκαν για λόγους παρουσίασης.

Οι ευαίσθητες πληροφορίες σύνδεσης του Phone Import έχουν κρυφτεί από το δημόσιο screenshot.

Καμία πραγματική ιδιωτική media library ή προσωπικά backup data δεν περιλαμβάνονται σε αυτό το repository.

---

## Source Code

Ο πλήρης production πηγαίος κώδικας του MyMediaManager διατηρείται ιδιωτικός.

Αυτό το δημόσιο repository χρησιμοποιείται αποκλειστικά ως **product showcase και portfolio παρουσίαση**.

Περιέχει documentation και οπτικό υλικό που παρουσιάζουν τη λειτουργικότητα της εφαρμογής.

Ο πλήρης production source code, η application database, η private media library, τα bundled recognition assets και τα internal application files δεν δημοσιεύονται εδώ.

---

## Κατάσταση Project

**Λειτουργικό Windows desktop software project.**

Το MyMediaManager είναι λειτουργική εφαρμογή και συνεχίζει να λαμβάνει βελτιώσεις σε usability, reliability και product functionality.

---

## Δημιουργός

Σχεδιασμός και ανάπτυξη: **Menelaos Tzatzanis**

© 2026 Menelaos Tzatzanis. All rights reserved.
