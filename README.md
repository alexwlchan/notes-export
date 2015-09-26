# notes-export

### Export HTML copies of your notes from Apple Notes

I have tested this on the OS X El Capitan GM and a few of the developer seeds (I can't remember which ones); it probably doesn't work on older versions.

To go in the other direction, see Steven Frank's [notes-import script](https://github.com/panicsteve/notes-import).

    --
    -- notes-export.scpt
    -- Alex Chan <alex@alexwlchan.net>
    --
    -- Export all the notes from Notes.app into a folder as HTML text.
    -- A very basic backup script.
    --
    -- Usage:
    --  * Open this file in Script Editor
    --  * Run
    --  * Select a folder to export files to
    --
    -- Output:
    --  * A collection of (Latin-1 encoded) HTML files
    --  * A list of attachment names for each note.
    --
    -- Known issues:
    --  * Only the names of attachments are exported, not the files
    --    themselves.  (Look for the files in
    --    ~Library/Group Containers/group.com.apple.notes/Media).
    --  * Some attachment types (e.g. app links) show up as "Missing value"
    --  * Some formatting is lost.
    --  * A note with the same title as a previously exported note will be
    --    overwritten.
    --  * It will exported notes in the "Recently Deleted" folder which
    --    haven't been purged from disk yet.
    --