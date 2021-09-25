---
title: Öffnen eines Nachrichtenspeicherordners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cdd271a72166204a7c1a2f6c23b00c31f3489455
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555972"
---
# <a name="opening-a-message-store-folder"></a>Öffnen eines Nachrichtenspeicherordners

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor ein Ordner geöffnet werden kann, muss der Eintragsbezeichner verfügbar sein. Für die meisten Ordner bedeutet dies, dass ihre **PR_ENTRYID** Eigenschaften abgerufen werden. Für spezielle Ordner, z. B. einige der IPM-Unterstrukturordner und andere Stammordner, definiert MAPI spezielle Eintragsbezeichnereigenschaften, auf die durch Aufrufen der **IMAPIProp::GetProps-Methode** des Nachrichtenspeichers zugegriffen werden kann. Diese Eintragsbezeichner sind immer langfristig und werden wie folgt benannt: 
  
|**Ordner**|**Eintragsbezeichnereigenschaft**|
|:-----|:-----|
|Postausgang  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (nur IPM-Nachrichtenklasse)  <br/> |
|Ordner "Gelöschte Elemente"  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|Ordner 'Gesendete Elemente'  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM-Stammordner  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Suchergebnisse Stammordner  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Stammordner für allgemeine Ansichten  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Stammordner für persönliche Ansichten  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Stammordner "Kontakte"  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Entwurfsstammordner  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Journalstammordner  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Kalenderstammordner  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Notizenstammordner  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Tasks-Stammordner  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Bevor Sie versuchen, einen dieser speziellen Eintragsbezeichner abzurufen, rufen Sie die **PR \_ VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) -Eigenschaft des Nachrichtenspeichers ab. **PR \_ VALID_FOLDER_MASK** ist eine Bitmaske, die angibt, welche der speziellen Eintragsbezeichner vorhanden sind. Es gibt ein Bit für jeden speziellen Ordner. Wenn das Bit festgelegt ist, gibt es an, dass der entsprechende Ordner unterstützt wird und über einen gültigen Eintragsbezeichner verfügt. Wenn beispielsweise der Ordner "Gelöschte Elemente" vorhanden ist und einen gültigen Eintragsbezeichner aufweist, wird das \_ FOLDER IPM_WASTEBASKET_VALID Bit in **PR_VALID_FOLDER_MASK** festgelegt. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Öffnen Des Ordners, in dem alle eingehenden Nachrichten einer bestimmten Klasse platziert werden
  
1. Rufen [Sie IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner abzurufen, und legen Sie den  _Parameter lpszMessageClass_ so fest, dass er auf eine Zeichenfolge verweist, die die Nachrichtenklasse identifiziert. Wenn Sie beispielsweise den Posteingang für Ihre IPM-Unterstruktur öffnen möchten, zeigen Sie  _lpszMessageClass_ auf IPM. Wenn Sie den Empfangsordner für IPC-Nachrichten öffnen möchten, legen Sie ihn so fest, dass er auf IPC verweist. 

   Wenn kein registrierter Empfangsordner für die Nachrichtenklasse vorhanden ist, wählt **GetReceiveFolder** den Empfangsordner aus, dessen zugeordnete Nachrichtenklasse dem längsten möglichen Präfix der übergebenen Nachrichtenklasse entspricht. Weitere Informationen finden Sie unter [MAPI Receive Folders](mapi-receive-folders.md). 
   
   Beachten Sie, dass die **eigenschaft PR_IPM_OUTBOX_ENTRYID** verwendet wird, um den Ordner "Postausgang" nur für IPM-Nachrichten zu öffnen. Wenn Sie den Postausgang für IPC-Nachrichten öffnen, verwenden Sie stattdessen den Eintragsbezeichner für den Empfangsordner. Sowohl eingehende als auch ausgehende IPC-Nachrichten werden im Empfangsordner abgelegt. 
    
2. Rufen Sie eine von vier **OpenEntry-Methoden** auf, um den Ordner zu öffnen und einen Schnittstellenzeiger zurückzugeben, mit dem Sie darauf zugreifen können. Sie können eine der folgenden Methoden aufrufen, um einen Ordner zu öffnen: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   Die spezifische Methode, die Sie auswählen, hängt vom zu öffnenden Ordner und den Objekten ab, die zu diesem Zeitpunkt verfügbar sind. Da die **IMAPISession-Methode** einen beliebigen Ordner für jeden Nachrichtenspeicher im aktuellen Profil öffnen kann, rufen Sie diesen **OpenEntry** auf, wenn Sie nichts über den zu öffnenden Ordner wissen. Wenn Sie wissen, welcher Nachrichtenspeicher den Ordner besitzt und Sie einen Zeiger auf den Nachrichtenspeicher haben, rufen Sie **IMsgStore::OpenEntry** auf. 
    
   Verwenden Sie beispielsweise die **IMsgStore-Methode,** um einen Empfangsordner zu öffnen. Wenn Sie einen Zeiger auf das Anmeldeobjekt des Nachrichtenspeicheranbieters haben, rufen Sie **IMSLogon::OpenEntry** auf. Da diese Aufrufe direkt an den Nachrichtenspeicheranbieter und nicht über die MAPI erfolgen, ist die Verarbeitung schneller. Wenn der Ordner, den Sie öffnen, ein Unterordner eines Ordners ist, den Sie bereits geöffnet haben, rufen Sie die **IMAPIContainer::OpenEntry-Methode** des geöffneten Ordners auf. Die **IMAPIContainer-Methode** öffnet nur Unterordner eines aktuell geöffneten Ordners und ist die einzige Methode, die garantiert mit kurzfristigen Eintragsbezeichnern funktioniert. 
    
3. Wenn Sie Änderungen am zu öffnenden Ordner vornehmen möchten, geben Sie eine Zugriffsebene an, indem Sie entweder das MAPI \_ BEST \_ ACCESS- oder MAPI \_ MODIFY-Flag im **OpenEntry-Aufruf** festlegen. Diese Flags sind Vorschläge für den Nachrichtenspeicheranbieter, beim Öffnen des Ordners die höchste Zugriffsebene zu gewähren, für MAPI \_ BEST \_ ACCESS oder Lese-/Schreibzugriff, für MAPI \_ MODIFY. 

   Da es sich bei diesen Flags nur um Vorschläge handelt, wird der Ordner möglicherweise mit der erwarteten Zugriffsebene geöffnet. Durch Abrufen der **eigenschaft PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) können Sie den Bereich der Vorgänge bestimmen, die für den geöffneten Ordner ausgeführt werden können. 
    
   Da jedoch viele Nachrichtenspeicheranbieter den Wert für diese Eigenschaft bei Bedarf berechnen, anstatt ihn als Ordnereigenschaft oder als Spalte in ihrer Hierarchietabelle zu unterstützen, kann das Abrufen dieser Eigenschaft zeitaufwändig sein. Eine alternative Strategie besteht darin, zu versuchen, welchen Vorgang Sie ausführen müssen, und bei Bedarf einen Fehler zurückzugeben.
    
## <a name="see-also"></a>Siehe auch

- [PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

