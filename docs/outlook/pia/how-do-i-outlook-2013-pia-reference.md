---
title: Gewusst wie... (Outlook 2013 PIA-Referenz)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bc4e19271e2747f5ffa8586b9f2ab226d6658b4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711721"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a>Gewusst wie... (Outlook 2013 PIA-Referenz)

Dieser Abschnitt enthält Themen zu Vorgehensweisen und Codebeispiele in Visual Basic und C\#, die die Ausführung einiger allgemeiner Aufgaben in Outlook veranschaulichen.

Zum Ausführen dieser Codebeispiele müssen Outlook 2010 und Visual Studio 2008 oder eine höhere Version dieser Produkte installiert sein.

Für die Codebeispiele in diesem Abschnitt müssen die Office Developer Tools für Visual Studio nicht installiert sein. Im Portal für den [Einstieg in die Office-Entwicklung](https://developer.microsoft.com/office/docs) finden Sie Informationen zur Verwendung der Tools. Unter [Outlook-Lösungen](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) finden Sie grundlegende Anleitungen, die in verwaltetem Code geschrieben wurden.

Die Codebeispiele in diesem Abschnitt reichen vom Anfänger- bis zum Fortgeschrittenenniveau, und einige basieren auf dem Buch [Programming Applications for Microsoft Office Outlook 2007 (Programmieren von Anwendungen für Microsoft Office Outlook 2007, in englischer Sprache)](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).

Das für die Office-Entwicklerdokumentation zuständige Team freut sich über Ihre Vorstellungen zu Aufgaben und Codebeispiele. Sollten wir Ihre Codebeispiele in Outlook-Inhalten verwenden, erkennen wir Ihre Arbeit mit einer Verfasserzeile und einem Link zu Ihrer Website an. Wenn Sie weitere Informationen wünschen, wenden Sie sich unter docthis@microsoft.com an uns.

## <a name="in-this-section"></a>Inhalt dieses Abschnitts 

[Konten](accounts.md)

- [Abrufen von Kontoinformationen](how-to-get-account-information.md)
- [Erstellen eines sendbaren Elements für ein bestimmtes Konto auf der Basis des aktuellen Ordners](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [Abrufen des Kontos für einen Ordner](how-to-get-the-account-for-a-folder.md)
- [Abrufen von Informationen über mehrere Konten](how-to-get-information-about-multiple-accounts.md)
- [Senden eines E-Mail-Elements mithilfe eines Hotmail-Kontos](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[Add-In-Verwaltung](add-in-administration.md)

- [Bestimmen, ob Outlook eine Klick-und-Los-Anwendung auf einem Computer ist](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[Adressbuch](address-book.md)

- [Anzeigen des Adressbuchs, das einem Ordner „Kontakte“ entspricht, im Dialogfeld „Namen auswählen“](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [Abrufen der globalen Adressliste oder eines Satzes von Adresslisten für einen Speicher](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [Aufzählen der Einträge in der globalen Adressliste](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [Anzeigen der Adresslisten für ein Profil](how-to-display-the-address-lists-for-a-profile.md)

[Termine](appointments.md)

- [Erstellen eines Termins, der ein ganztägiges Ereignis darstellt](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [Erstellen eines Termins mit Startzeit in der Pacific Time-Zone und Endzeit in der Eastern Time-Zone](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [Angeben verschiedener Empfängertypen für ein Terminelement](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [Erstellen einer Terminserie mithilfe des Standardserienmusters](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [Erstellen einer Terminserie mit einem wöchentlichen Muster](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [Erstellen einer jährlichen Terminserie mit einem YearNth-Muster](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [Suchen nach einem bestimmten Termin in einer Terminserie](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [Erstellen eines Ausnahmetermins in einer Terminserie](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [Erstellen einer Erinnerung für ein Terminelement](how-to-create-a-reminder-for-an-appointment-item.md)
- [Importieren von Termin-XML-Daten in Outlook-Terminobjekte](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[Anlagen](attachments.md)

- [Anhängen einer Datei an eine E-Mail-Nachricht](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [Anfügen eines Outlook-Kontaktelements an eine E-Mail-Nachricht](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [Beschränken der Größe einer Anlage für eine Outlook-E-Mail-Nachricht](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [Ändern einer Anlage einer Outlook-E-Mail](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [Programmgesteuertes Entfernen von Anlagen der Sicherheitsstufe 2 aus Nachrichten und Speichern der Anlagen auf einem Datenträger](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[Kalender](calendar.md)

- [Freigeben eines Frei-/Gebucht-Zeitplans innerhalb eines bestimmten Zeitraums in einem Kalender](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [Freigeben von Kalenderinformationen per E-Mail](how-to-share-calendar-information-through-e-mail.md)
- [Anzeigen eines freigegebenen Kalenders eines Empfängers](how-to-display-a-shared-calendar-of-a-recipient.md)
- [Speichern eines Kalenders auf einem Datenträger](how-to-save-a-calendar-to-disk.md)
- [Öffnen und Anzeigen des Inhalts einer iCalendar-Datei](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[Farbkategorien](color-categories.md)

- [Aufzählen und Hinzufügen von Kategorien](how-to-enumerate-and-add-categories.md)
- [Zuweisen von Kategorien zu einem Element](how-to-assign-categories-to-an-item.md)

[Kontakte](contacts.md)

- [Erstellen eines Kontaktelements](how-to-create-a-contact-item.md)
- [Erstellen eines benutzerdefinierten Kontaktelements](how-to-create-a-custom-contact-item.md)
- [Erstellen eines Kontaktelements aus einer vCard-Datei und Speichern des Elements in einem Ordner](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[Unterhaltungen](conversations.md)

- [Abrufen und Anzeigen von Elementen in einer Unterhaltung](how-to-get-and-display-items-in-a-conversation.md)
- [Abrufen und Aufzählen von ausgewählten Unterhaltungen](how-to-get-and-enumerate-selected-conversations.md)

[Elektronische Visitenkarten](electronic-business-cards.md)

- [Ändern des Layouts einer elektronischen Visitenkarte](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [Senden eines E-Mail-Elements mit einer elektronischen Visitenkarte](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[Exchange-Benutzer](exchange-users.md)

- [Abrufen von Informationen über den aktuellen Benutzer](how-to-get-information-about-the-current-user.md)
- [Abrufen von Informationen über alle Verteilerlisten, in denen der aktuelle Benutzer Mitglied ist](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [Erstellen einer Verteilerliste](how-to-create-a-distribution-list.md)
- [Abrufen der Mitglieder einer Exchange-Verteilerliste](how-to-get-members-of-an-exchange-distribution-list.md)
- [Abrufen von Informationen zum Vorgesetzten des aktuellen Benutzers](how-to-get-information-about-the-current-user-s-manager.md)
- [Abrufen von Verfügbarkeitsinformationen für den Vorgesetzten eines Exchange-Benutzers](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [Überprüfen der Antwort eines Vorgesetzten auf eine Besprechungsanfrage](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [Abrufen von Informationen zu direkten Mitarbeitern des Vorgesetzten des aktuellen Benutzers](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[Ordner](folders.md)

- [Hinzufügen eines Ordners zur Ordnerliste](how-to-add-a-folder-to-the-folder-list.md)
- [Aufzählen von Ordnern](how-to-enumerate-folders.md)
- [Abrufen eines Standardordners und Auflisten seiner Unterordner](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [Abrufen eines Ordners basierend auf seinem Ordnerpfad](how-to-get-a-folder-based-on-its-folder-path.md)
- [Auswählen eines Ordners und Anzeigen von Ordnerinformationen](how-to-select-a-folder-and-display-folder-information.md)
- [Abrufen der Standardnachrichtenklasse eines Ordners](how-to-get-the-default-message-class-of-a-folder.md)
- [Zugreifen auf lösungsspezifische Daten, die als ausgeblendete Nachricht in einem Ordner gespeichert sind](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [Sicherstellen, dass benutzerdefinierte Elementeigenschaften in Abfragen auf Ordnerebene unterstützt werden](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[Allgemeine Outlook-Elemente](general-outlook-items.md)

- [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Anzeigen von ausgewählten Elementen im aktiven Explorer](how-to-display-selected-items-in-the-active-explorer.md)

[Gruppenfreigabe](group-sharing.md)

- [Abonnieren eines RSS-Feeds](how-to-subscribe-to-an-rss-feed.md)
- [Synchronisieren von Outlook mit einem SharePoint-Ordner](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[Mail](mail.md)

- [Erstellen eines E-Mail-Elements mithilfe einer Nachrichtenvorlage](how-to-create-a-mail-item-by-using-a-message-template.md)
- [Erstellen eines E-Mail-Elements, Anfügen eines Berichts und Senden des E-Mail-Elements an den Vorgesetzten des Benutzers](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [Senden einer E-Mail-Nachricht mithilfe der SMTP-Adresse eines Kontos](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [Hinzufügen von Abstimmungsoptionen zu einem E-Mail-Element](how-to-add-voting-options-to-a-mail-item.md)
- [Hinzufügen einer benutzerdefinierten Aktion als Antwort auf ein E-Mail-Element](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [Abrufen der SMTP-Adresse des Absenders eines E-Mail-Elements](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [Angeben verschiedener Empfängertypen für ein E-Mail-Element](how-to-specify-different-recipient-types-for-a-mail-item.md)

[Besprechungsanfragen](meeting-requests.md)

- [Erstellen einer Besprechungsanfrage, Hinzufügen von Empfängern und Angeben eines Orts](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [Abrufen des Organisators einer Besprechung](how-to-get-the-organizer-of-a-meeting.md)
- [Überprüfen aller Antworten auf eine Besprechungsanfrage](how-to-check-all-responses-to-a-meeting-request.md)
- [Suchen des einer Besprechungsanfrage zugeordneten Terminelements](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [Automatisches Annehmen einer Besprechungsanfrage](how-to-automatically-accept-a-meeting-request.md)
- [Auffordern eines Benutzers zum Antworten auf eine Besprechungsanfrage](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[Empfänger](recipients.md)

- [Anzeigen des Dialogfelds „Namen auswählen“ zum Auflösen von Empfängern](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [Verwenden des Dialogfelds „Namen auswählen“ zum Abrufen und Zuweisen von Empfängern zu einem Termin](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [Abrufen der E-Mail-Adresse eines Empfängers](how-to-get-the-e-mail-address-of-a-recipient.md)

[Regeln](rules.md)

- [Erstellen einer Regel zum Ablegen von E-Mail-Elementen von einem Vorgesetzten und Kennzeichnen dieser Elemente für die Nachverfolgung](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [Sofortiges Ausführen einer Regel](how-to-execute-a-rule-instantly.md)
- [Ausführen einer Regel auf einem lokalen Computer](how-to-execute-a-rule-on-a-local-computer.md)
- [Erstellen einer Regel zum Zuweisen von Kategorien zu E-Mail-Elementen basierend auf mehreren Wörtern im Betreff](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[Beispielaufgaben mit Outlook-Ereignissen](sample-tasks-using-outlook-events.md)

- [Implementieren eines Wrappers für Prüfungen und Nachverfolgung von Ereignissen auf Elementebene in jedem Inspektor](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[Suchen und Filtern](search-and-filter.md)

- [Filtern und effizientes Aufzählen von Elementen in einem Ordner](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [Verwenden von SetColumns zum effizienten Aufzählen von Elementen in einem Ordner](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [Verwenden von Arrays zum effizienten Aufzählen von Elementen in einem Ordner](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [Aufzählen der Elemente im Posteingang basierend auf dem Zeitpunkt der letzten Änderung](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [Filtern und Anzeigen der im letzten Monat geänderten Posteingangselemente](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [Filtern und Anzeigen von mehrwertigen Eigenschaften beim Aufzählen von Elementen in einem Ordner](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [Filtern und Anzeigen von berechneten Eigenschaften beim Aufzählen von Elementen in einem Ordner](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [Aufzählen von ausgeblendeten Elementen in einem Ordner](how-to-enumerate-hidden-items-in-a-folder.md)
- [Verwenden der Sofortsuche zum Durchsuchen aller Ordner und aller Stores nach einem Ausdruck im Betreff](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [Suchen nach einem Ausdruck im Textkörper von Elementen in einem Ordner](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [Durchsuchen der Anlagen von Elementen in einem Ordner nach einem exakten Ausdruck](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [Suchen und Abrufen von Terminen in einem Zeitbereich](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [Filtern von Terminserien und Suchen nach einer Zeichenfolge im Betreff](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [Suchen und Abrufen von Elementen in einer aggregierten Ansicht](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[Sitzungen](sessions.md)

- [Abrufen einer Instanz von Outlook und Anmelden bei dieser](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[Speicher](stores.md)

- [Abrufen von Informationen zu Speichern in einem Profil](how-to-get-information-about-stores-in-a-profile.md)
- [Hinzufügen oder Entfernen eines Speichers](how-to-add-or-remove-a-store.md)

[Aufgaben](tasks.md)

- [Erstellen eines Aufgabenelements](how-to-create-a-task-item.md)
- [Zuordnen einer Aufgabe zu einem Empfänger](how-to-assign-a-task-to-a-recipient.md)
- [Anzeigen der an einen Empfänger gesendeten Aufgabenanforderungselemente](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [Antworten auf ein Aufgabenanforderungselement](how-to-respond-to-a-task-request-item.md)
- [Erstellen eines periodischen Vorgangs](how-to-create-a-recurring-task.md)
- [Kennzeichnen von E-Mail-Elementen von einem Vorgesetzten zur Nachverfolgung](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[Ansichten](views.md)

- [Erstellen einer Ansicht](how-to-create-a-view.md)
- [Hinzufügen von Feldern zu einer Ansicht](how-to-add-fields-to-a-view.md)
- [Auflisten der Elemente in einer Tabellenansicht](how-to-enumerate-items-in-a-table-view.md)



