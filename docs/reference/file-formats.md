# file-formats

## `$alias_format`

| Expando | Description                                                     |
| :------ | :-------------------------------------------------------------- |
| `%a`    | Alias name                                                      |
| `%A`    | Full Address (Name and Email)                                   |
| `%C`    | Comment                                                         |
| `%E`    | Email Address                                                   |
| `%f`    | Flags - currently, a `d` for an alias marked for deletion       |
| `%i`    | Index number                                                    |
| `%N`    | Real name                                                       |
| `%t`    | Alias is tagged (selected)                                      |
| `%Y`    | User-defined tags (labels)                                      |
| `%>X`   | right justify the rest of the string and pad with character `X` |
| `%\|X`  | pad to the end of the line with character `X`                   |
| `%*X`   | soft-fill with character `X` as pad                             |

## `$alias_format` deprecated

| Expando | Description    |
| :------ | :------------- |
| `%c`    | Use %C instead |
| `%n`    | Use %i instead |
| `%r`    | Use %A instead |

## `$attach_format`

| Expando | Description                                                        |
| :------ | :----------------------------------------------------------------- |
| `%C`    | Charset                                                            |
| `%c`    | Requires charset conversion (`n` or `c`)                           |
| `%D`    | Deleted flag                                                       |
| `%d`    | Description (if none, falls back to %F)                            |
| `%e`    | MIME content-transfer-encoding                                     |
| `%f`    | Filename                                                           |
| `%F`    | Filename in content-disposition header (if none, falls back to %f) |
| `%I`    | Disposition (`I` for inline, `A` for attachment)                   |
| `%m`    | Major MIME type                                                    |
| `%M`    | MIME subtype                                                       |
| `%n`    | Attachment number                                                  |
| `%Q`    | `Q`, if MIME part qualifies for attachment counting                |
| `%s`    | Size (see $formatstrings-size)                                     |
| `%T`    | Graphic tree characters                                            |
| `%t`    | Tagged flag                                                        |
| `%u`    | Unlink (=to delete) flag                                           |
| `%X`    | Number of qualifying MIME parts in this part and its children      |
| `%>X`   | Right justify the rest of the string and pad with character `X`    |
| `%\|X`  | Pad to the end of the line with character `X`                      |
| `%*X`   | Soft-fill with character `X` as pad                                |

## `$autocrypt_acct_format`

| Expando | Description                                                     |
| :------ | :-------------------------------------------------------------- |
| `%a`    | email address                                                   |
| `%k`    | gpg keyid                                                       |
| `%n`    | current entry number                                            |
| `%p`    | prefer-encrypt flag                                             |
| `%s`    | status flag (active/inactive)                                   |
| `%>X`   | right justify the rest of the string and pad with character `X` |
| `%\|X`  | pad to the end of the line with character `X`                   |
| `%*X`   | soft-fill with character `X` as pad                             |

## `$compose_format`

| Expando | Description                                                                  |
| :------ | :--------------------------------------------------------------------------- |
| `%a`    | Total number of attachments                                                  |
| `%h`    | Local hostname                                                               |
| `%l`    | Approximate size (in bytes) of the current message (see $formatstrings-size) |
| `%v`    | NeoMutt version string                                                       |
| `%>X`   | right justify the rest of the string and pad with character `X`              |
| `%\|X`  | pad to the end of the line with character `X`                                |
| `%*X`   | soft-fill with character `X` as pad                                          |

## `$folder_format`

| Expando  | Flags | Description                                                              |
| :------- | :---- | :----------------------------------------------------------------------- |
| `%a`     |       | Alert: 1 if user is notified of new mail                                 |
| `%C`     |       | Current file number                                                      |
| `%d`     |       | Date/time folder was last modified                                       |
| `%D`     |       | Date/time folder was last modified using `$date_format`                  |
| `%f`     |       | Filename (`/` is appended to directory names,                            |
| `%F`     |       | File permissions                                                         |
| `%g`     |       | Group name (or numeric gid, if missing)                                  |
| `%i`     |       | Description of the folder                                                |
| `%l`     |       | Number of hard links                                                     |
| `%m`     | \*    | Number of messages in the mailbox                                        |
| `%n`     | \*    | Number of unread messages in the mailbox                                 |
| `%N`     |       | `N` if mailbox has new mail, ` ` (space) otherwise                       |
| `%p`     |       | Poll: 1 if Mailbox is checked for new mail                               |
| `%s`     |       | Size in bytes (see $formatstrings-size)                                  |
| `%t`     |       | `\*` if the file is tagged, blank otherwise                              |
| `%u`     |       | Owner name (or numeric uid, if missing)                                  |
| `%[fmt]` |       | Date/time folder was last modified using an `strftime(3)` expression     |
| `%>X`    |       | Right justify the rest of the string and pad with character `X`          |
| `%\|X`   |       | Pad to the end of the line with character `X`                            |
| `%*X`    |       | Soft-fill with character `X` as pad                                      |

\* = can be optionally printed if nonzero

## `$greeting`

| Expando | Description                    |
| :------ | :----------------------------- |
| `%n`    | Recipient's real name          |
| `%u`    | User (login) name of recipient |
| `%v`    | First name of recipient        |

## `$group_index_format`

| Expando | Description                                                        |
| :------ | :----------------------------------------------------------------- |
| `%a`    | Alert: 1 if user is notified of new mail                           |
| `%C`    | Current newsgroup number                                           |
| `%d`    | Description of newsgroup (becomes from server)                     |
| `%f`    | Newsgroup name                                                     |
| `%M`    | - if newsgroup not allowed for direct post (moderated for example) |
| `%N`    | N if newsgroup is new, u if unsubscribed, blank otherwise          |
| `%n`    | Number of new articles in newsgroup                                |
| `%p`    | Poll: 1 if Mailbox is checked for new mail                         |
| `%s`    | Number of unread articles in newsgroup                             |
| `%>X`   | Right justify the rest of the string and pad with character `X`    |
| `%\|X`  | Pad to the end of the line with character `X`                      |
| `%*X`   | Soft-fill with character `X` as pad                                |

## `$history_format`

| Expando | Description                                                     |
| :------ | :-------------------------------------------------------------- |
| `%C`    | Line number                                                     |
| `%s`    | History match                                                   |
| `%>X`   | right justify the rest of the string and pad with character `X` |
| `%\|X`  | pad to the end of the line with character `X`                   |
| `%*X`   | soft-fill with character `X` as pad                             |

## `$indent_string`

| Expando   | Description                                                                                     |
| :-------- | :---------------------------------------------------------------------------------------------- |
| `%a`      | Address of the author                                                                           |
| `%A`      | Reply-to address (if present; otherwise: address of author)                                     |
| `%b`      | Filename of the original message folder (think mailbox)                                         |
| `%B`      | Same as %K                                                                                      |
| `%c`      | Number of characters (bytes) in the body of the message (see $formatstrings-size)               |
| `%C`      | Current message number                                                                          |
| `%cr`     | Number of characters (bytes) in the raw message, including the header (see $formatstrings-size) |
| `%d`      | Date and time of message using `$date_format` and sender's timezone                             |
| `%D`      | Date and time of message using `$date_format` and local timezone                                |
| `%e`      | Current message number in thread                                                                |
| `%E`      | Number of messages in current thread                                                            |
| `%f`      | Sender (address + real name), either From: or Return-Path:                                      |
| `%F`      | Author name, or recipient name if the message is from you                                       |
| `%Fp`     | Like %F, but plain. No contextual formatting is applied to recipient name                       |
| `%g`      | Message tags (e.g. notmuch tags/imap flags)                                                     |
| `%Gx`     | Individual message tag (e.g. notmuch tags/imap flags)                                           |
| `%H`      | Spam attribute(s) of this message                                                               |
| `%i`      | Message-id of the current message                                                               |
| `%I`      | Initials of author                                                                              |
| `%J`      | Message tags (if present, tree unfolded, and != parent's tags)                                  |
| `%K`      | The list to which the letter was sent (if any; otherwise: empty)                                |
| `%l`      | number of lines in the unprocessed message (may not work with                                   |
| `%L`      | If an address in the `To:` or `Cc:` header field matches an address                             |
| `%m`      | Total number of message in the mailbox                                                          |
| `%M`      | Number of hidden messages if the thread is collapsed                                            |
| `%n`      | Author's real name (or address if missing)                                                      |
| `%N`      | Message score                                                                                   |
| `%O`      | Original save folder where NeoMutt would formerly have                                          |
| `%P`      | Progress indicator for the built-in pager (how much of the file has been displayed)             |
| `%q`      | Newsgroup name (if compiled with NNTP support)                                                  |
| `%r`      | Comma separated list of `To:` recipients                                                        |
| `%R`      | Comma separated list of `Cc:` recipients                                                        |
| `%s`      | Subject of the message                                                                          |
| `%S`      | Single character status of the message (`N`/`O`/`D`/`d`/`!`/`r`/`*`)                            |
| `%t`      | `To:` field (recipients)                                                                        |
| `%T`      | The appropriate character from the `$to_chars` string                                           |
| `%u`      | User (login) name of the author                                                                 |
| `%v`      | First name of the author, or the recipient if the message is from you                           |
| `%W`      | Name of organization of author (`Organization:` field)                                          |
| `%x`      | `X-Comment-To:` field (if present and compiled with NNTP support)                               |
| `%X`      | Number of MIME attachments                                                                      |
| `%y`      | `X-Label:` field, if present                                                                    |
| `%Y`      | `X-Label:` field, if present, and \fI(1)\fP not at part of a thread tree,                       |
| `%Z`      | A three character set of message status flags                                                   |
| `%zc`     | Message crypto flags                                                                            |
| `%zs`     | Message status flags                                                                            |
| `%zt`     | Message tag flags                                                                               |
| `%@name@` | insert and evaluate format-string from the matching                                             |
| `%{fmt}`  | the date and time of the message is converted to sender's                                       |
| `%[fmt]`  | the date and time of the message is converted to the local                                      |
| `%(fmt)`  | the local date and time when the message was received, and                                      |
| `%>X`     | right justify the rest of the string and pad with character `X`                                 |
| `%\|X`    | pad to the end of the line with character `X`                                                   |
| `%*X`     | soft-fill with character `X` as pad                                                             |

## `$newsrc`

| Expando | Description       | Example               |
| :------ | :---------------- | :-------------------- |
| `%a`    | Account url       | `news:news.gmane.org` |
| `%p`    | Port              | `119`                 |
| `%P`    | Port if specified | `10119`               |
| `%s`    | News server name  | `news.gmane.org`      |
| `%S`    | Url schema        | `news`                |
| `%u`    | Username          | `username`            |

## `$pattern_format`

| Expando | Description                                                     |
| :------ | :-------------------------------------------------------------- |
| `%d`    | pattern description                                             |
| `%e`    | pattern expression                                              |
| `%n`    | index number                                                    |
| `%>X`   | right justify the rest of the string and pad with character `X` |
| `%\|X`  | pad to the end of the line with character `X`                   |
| `%*X`   | soft-fill with character `X` as pad                             |

## `$pgp_decode_command`

| Expando | Description                                                      |
| :------ | :--------------------------------------------------------------- |
| `%a`    | The value of `$pgp_sign_as` if set, otherwise the value          |
| `%f`    | Expands to the name of a file containing a message               |
| `%p`    | Expands to PGPPASSFD=0 when a pass phrase is needed, to an empty |
| `%r`    | One or more key IDs (or fingerprints if available)               |
| `%s`    | Expands to the name of a file containing the signature part      |

## `$pgp_entry_format`

| Expando  | Description                                                     |
| :------- | :-------------------------------------------------------------- |
| `%a`     | Algorithm                                                       |
| `%c`     | Capabilities                                                    |
| `%f`     | Flags                                                           |
| `%i`     | Key fingerprint (or long key id if non-existent)                |
| `%k`     | Key id                                                          |
| `%l`     | Key length                                                      |
| `%n`     | Number                                                          |
| `%p`     | Protocol                                                        |
| `%t`     | Trust/validity of the key-uid association                       |
| `%u`     | User id                                                         |
| `%[<s>]` | Date of the key where `<s>` is an \fCstrftime(3)\fP expression  |
| `%>X`    | Right justify the rest of the string and pad with character `X` |
| `%\|X`   | Pad to the end of the line with character `X`                   |
| `%*X`    | Soft-fill with character `X` as pad                             |

## `$query_format`

| Expando | Description                                           |
| :------ | :---------------------------------------------------- |
| `%A`    | Full Address (Name and Email)                         |
| `%C`    | Comment                                               |
| `%E`    | Email Address                                         |
| `%i`    | Index number                                          |
| `%N`    | Real name                                             |
| `%t`    | Alias is tagged (selected)                            |
| `%Y`    | User-defined tags (labels)                            |
| `%>X`   | Right justify the rest of the string and pad with `X` |
| `%\|X`  | Pad to the end of the line with `X`                   |
| `%*X`   | Soft-fill with character `X` as pad                   |

## `$query_format` deprecated

| Expando | Description    |
| :------ | :------------- |
| `%a`    | Use %E instead |
| `%c`    | Use %i instead |
| `%e`    | Use %C instead |
| `%n`    | Use %N instead |

## `$sidebar_format`

| Expando | Flag | Flag | Description                                               |
| :------ | :--- | :--- | :-------------------------------------------------------- |
| `%a`    |      |      | Alert: 1 if user is notified of new mail                  |
| `%B`    |      |      | Name of the mailbox                                       |
| `%d`    | \*   | @    | Number of deleted messages in the mailbox                 |
| `%D`    |      |      | Descriptive name of the mailbox                           |
| `%F`    | \*   |      | Number of flagged messages in the mailbox                 |
| `%L`    | \*   | @    | Number of messages after limiting                         |
| `%n`    |      |      | `N` if mailbox has new mail, ` ` (space) otherwise        |
| `%N`    | \*   |      | Number of unread messages in the mailbox (seen or unseen) |
| `%o`    | \*   |      | Number of old messages in the mailbox (unread, seen)      |
| `%p`    |      |      | Poll: 1 if Mailbox is checked for new mail                |
| `%r`    | \*   |      | Number of read messages in the mailbox (read, seen)       |
| `%S`    | \*   |      | Size of mailbox (total number of messages)                |
| `%t`    | \*   | @    | Number of tagged messages in the mailbox                  |
| `%Z`    | \*   |      | Number of new messages in the mailbox (unread, unseen)    |
| `%!`    |      |      | `!` : one flagged message;                                |
| `%>X`   |      |      | Right justify the rest of the string and pad with `X`     |
| `%\|X`  |      |      | Pad to the end of the line with `X`                       |
| `%*X`   |      |      | Soft-fill with character `X` as pad                       |

\* = Can be optionally printed if nonzero
@ = Only applicable to the current folder

## `$smime_decrypt_command`

| Expando | Description                                                          |
| :------ | :------------------------------------------------------------------- |
| `%a`    | The algorithm used for encryption                                    |
| `%c`    | One or more certificate IDs                                          |
| `%C`    | CA location:  Depending on whether `$smime_ca_location`              |
| `%d`    | The message digest algorithm specified with `$smime_sign_digest_alg` |
| `%f`    | Expands to the name of a file containing a message                   |
| `%i`    | Intermediate certificates                                            |
| `%k`    | The key-pair specified with `$smime_default_key`                     |
| `%s`    | Expands to the name of a file containing the signature part          |

## `$status_format`

| Expando | Flag | Description                                                        |
| :------ | :--- | :----------------------------------------------------------------- |
| `%b`    | \*   | Number of mailboxes with new mail                                  |
| `%d`    | \*   | Number of deleted messages                                         |
| `%D`    |      | Description of the mailbox                                         |
| `%f`    |      | The full pathname of the current mailbox                           |
| `%F`    | \*   | Number of flagged messages                                         |
| `%h`    |      | Local hostname                                                     |
| `%l`    | \*   | Size (in bytes) of the current mailbox (see $formatstrings-size)   |
| `%L`    | \*   | Size (in bytes) of the messages shown                              |
| `%m`    | \*   | The number of messages in the mailbox                              |
| `%M`    | \*   | The number of messages shown (i.e., which match the current limit) |
| `%n`    | \*   | Number of new messages in the mailbox (unread, unseen)             |
| `%o`    | \*   | Number of old messages in the mailbox (unread, seen)               |
| `%p`    | \*   | Number of postponed messages                                       |
| `%P`    |      | Percentage of the way through the index                            |
| `%r`    |      | Modified/read-only/won't-write/attach-message indicator,           |
| `%R`    | \*   | Number of read messages in the mailbox (read, seen)                |
| `%s`    |      | Current sorting mode (`$sort`)                                     |
| `%S`    |      | Current aux sorting method (`$sort_aux`)                           |
| `%t`    | \*   | Number of tagged messages in the mailbox                           |
| `%T`    | \*   | Current threading mode (`$use_threads`)                            |
| `%u`    | \*   | Number of unread messages in the mailbox (seen or unseen)          |
| `%v`    |      | NeoMutt version string                                             |
| `%V`    | \*   | Currently active limit pattern, if any                             |
| `%>X`   |      | Right justify the rest of the string and pad with `X`              |
| `%\|X`  |      | Pad to the end of the line with `X`                                |
| `%*X`   |      | Soft-fill with character `X` as pad                                |

\* = can be optionally printed if nonzero

