---
title: Öffnen einen Speicherordner Nachricht
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 63b8224ad56e2b9985c9d733e2a3c27c67eb2f7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793309"
---
# <a name="opening-a-message-store-folder"></a>Öffnen einen Speicherordner Nachricht

**Betrifft**: Outlook 
  
Bevor ein beliebiger Ordner geöffnet werden kann, muss die Eintrags-ID verfügbar sein. Für die meisten Ordner bedeutet dies, deren Eigenschaften **PR_ENTRYID** abrufen. Für spezielle Ordner wie einiger der IPM Unterstruktur Ordnern und anderen Stammordner definiert MAPI spezieller Eintrag Bezeichnereigenschaften, die zugegriffen werden durch Aufrufen der Nachrichtenspeicher **IMAPIProp::GetProps** -Methode. Diese Eintragsbezeichner sind immer langfristige und heißen wie folgt: 
  
|**Folder**|**Eintrags-ID-Eigenschaft**|
|:-----|:-----|
|Postausgang  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Nur Nachrichtenklasse IPM)  <br/> |
|Ordner "Gel�schte Elemente"  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|Ordner 'Gesendete Elemente'  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM-Stammordner  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Suchergebnisse Stammordner  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Allgemeine Ansichten Stammordner  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Persönliche Ansichten Stammordner  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Stammordner für Kontakte  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Entwürfe Stammordner  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Journal-Stammordner  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Kalender-Stammordner  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Notes-Stammordner  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Stammordner Aufgaben  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Bevor Sie versuchen, eine der folgenden speziellen-Eintragsbezeichner abzurufen, Abrufen der **PR\_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))-Eigenschaft des Nachrichtenspeichers. **PR\_VALID_FOLDER_MASK** ist eine Bitmaske, die angibt, die von den Eintrag spezielle Bezeichner vorhanden. Ein Bit für jeden Ordner mit Sonderfunktion verwendet wird. Wenn das Bit festgelegt ist, bedeutet dies, dass der entsprechende Ordner unterstützt wird und verfügt über eine gültige Eingabe-Bezeichner. Beispielsweise, wenn der Ordner Gelöschte Objekte vorhanden ist und eine gültige Eintrags-ID, den Ordner\_IPM_WASTEBASKET_VALID Bit in **PR_VALID_FOLDER_MASK**festgelegt. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Öffnen Sie den Ordner, in dem alle eingehende Nachrichten von einer bestimmten Klasse platziert werden
  
1. Rufen Sie [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) zum Abrufen der Eintrags-ID, wenn der Parameter _LpszMessageClass_ So zeigen Sie auf eine Zeichenfolge, die die Nachrichtenklasse identifiziert. Angenommen, wenn Sie den Posteingang für IPM-Unterstruktur öffnen möchten, zeigen Sie _LpszMessageClass_ auf IPM. Wenn Sie den Empfangsordner für Nachrichten IPK öffnen möchten, legen Sie es so zeigen Sie auf IPK. 

   Wenn keine registrierten Empfangsordner für die Nachrichtenklasse vorhanden ist, wählt **GetReceiveFolder** übergeben der Empfangsordner, deren zugehörige Nachrichtenklasse das am längsten Präfix der Nachrichtenklasse übereinstimmt. Weitere Informationen finden Sie unter [Empfangen MAPI-Ordnern](mapi-receive-folders.md). 
   
   Beachten Sie, dass die **PR_IPM_OUTBOX_ENTRYID** -Eigenschaft zum Öffnen des Ordners Postausgang nur für IPM-Nachrichten verwendet wird. Wenn Sie im Ordner Postausgang für IPK Nachrichten öffnen, verwenden Sie stattdessen die Eintrags-ID für den Ordner erhalten. Eingehende und ausgehende IPK Nachrichten werden in den Empfangsordner abgelegt. 
    
2. Rufen Sie eine der vier **OpenEntry** Methoden öffnen Sie den Ordner und Zurückgeben eines Schnittstelle Zeigers, den Sie verwenden können, darauf zugreifen. Rufen Sie eine der folgenden Methoden, um einen Ordner zu öffnen: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   Die jeweilige Methode, die Sie auswählen, hängt davon ab, den Ordner geöffnet werden soll und die Objekte, die zum Zeitpunkt zur Verfügung stehen. Da die **IMAPISession** -Methode ein beliebiger Ordner für alle Nachrichtenspeicher im aktuellen Profil öffnen kann, rufen Sie diese **OpenEntry** , wenn Sie nicht wissen, über den Ordner geöffnet werden soll. Wenn Sie wissen, welche Nachrichtenspeicher der Besitzer des Ordners, und Sie einen Zeiger auf den Nachrichtenspeicher haben, rufen Sie **IMsgStore::OpenEntry**. 
    
   Verwenden Sie beispielsweise die **IMsgStore** -Methode, um eine Empfangsordner zu öffnen. Wenn Sie einen Zeiger auf die Nachricht Speicheranbieter Anmeldung-Objekt haben, rufen Sie **IMSLogon::OpenEntry**. Da diese Anrufe direkt an der Nachricht Informationsdienst nicht über MAPI ausgeführt werden, ist Verarbeitung schneller. Wenn der Ordner, den Sie öffnen möchten ein Unterordner eines Ordners ist, dass Sie bereits geöffnet ist, rufen Sie den Ordner öffnen **IMAPIContainer::OpenEntry** -Methode. Die **IMAPIContainer** -Methode öffnet nur Unterordner eines geöffneten Ordners und ist die einzige Methode kurzfristige-Eintragsbezeichner entwickelt. 
    
3. Wenn Sie Änderungen vorzunehmen, zu dem Ordner geöffnet werden können möchten, geben Sie eine Zugriffsebene durch Festlegen der entweder MAPI\_BEWÄHRTE\_ACCESS als auch die MAPI\_Flag in den Anruf **OpenEntry** ändern. Diese Flags sind Vorschläge auf die Nachricht-Anbieter die höchste Zugriffsebene, für die MAPI erteilen\_BEWÄHRTE\_Zugriff oder Lese-/Schreibzugriff für die MAPI\_zu ändern, wenn Sie den Ordner zu öffnen. 

   Da diese Flags nur Vorschläge sind, wird der Ordner möglicherweise oder kann nicht geöffnet werden, mit der Zugriffsebene, die Sie erwarten. Durch die Eigenschaft **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) abrufen, können Sie den Bereich der Vorgänge ermitteln, die für den Ordner öffnen ausgeführt werden kann. 
    
   Allerdings, da viele Nachricht-Anbieter den Wert für diese Eigenschaft bei Bedarf, statt ihn als ein Folder-Eigenschaft oder eine Spalte in ihrer Hierarchietabelle unterstützt berechnen, können sie abrufen zeitaufwendig sein. Eine alternative Strategie besteht darin, den Vorgang versuchen müssen Sie ausführen und einen Fehler zurück, falls erforderlich.
    
## <a name="see-also"></a>Siehe auch

- [PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

