---
title: Öffnen eines Nachrichtenspeicherordners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436538"
---
# <a name="opening-a-message-store-folder"></a>Öffnen eines Nachrichtenspeicherordners

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor ein Ordner geöffnet werden kann, muss der Eintragsbezeichner verfügbar sein. Für die meisten Ordner bedeutet dies, dass die PR_ENTRYID **abgerufen** werden. Für spezielle Ordner, z. B. einige der IPM-Unterstrukturordner und andere Stammordner, definiert MAPI spezielle Eintrags-ID-Eigenschaften, auf die zugegriffen werden kann, indem die **IMAPIProp::GetProps-Methode des Nachrichtenspeichers aufruft.** Diese Eintragsbezeichner sind immer langfristig und werden wie folgt benannt: 
  
|**Folder**|**Entry Identifier-Eigenschaft**|
|:-----|:-----|
|Postausgang  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (nur IPM-Nachrichtenklasse)  <br/> |
|Ordner "Gelöschte Elemente"  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|Ordner 'Gesendete Elemente'  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM-Stammordner  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Suchergebnisse Stammordner  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Stammordner für allgemeine Ansichten  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Stammordner für persönliche Ansichten  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Stammordner "Kontakte"  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Entwurf eines Stammordners  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Stammordner des Journals  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Kalenderstammordner  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Notes-Stammordner  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Aufgabenstammordner  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Bevor Sie versuchen, eine dieser speziellen Eintragsbezeichner abzurufen, rufen Sie die **\_ PR-VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) -Eigenschaft des Nachrichtenspeichers ab. **PR \_ VALID_FOLDER_MASK** ist eine Bitmaske, die identifiziert, welche der speziellen Eintragsbezeichner vorhanden ist. Für jeden speziellen Ordner gibt es ein Bit. Wenn das Bit festgelegt ist, gibt es an, dass der entsprechende Ordner unterstützt wird und über einen gültigen Eintragsbezeichner verfügt. Wenn beispielsweise der Ordner "Gelöschte Elemente" vorhanden ist und über einen gültigen Eintragsbezeichner verfügt, wird IPM_WASTEBASKET_VALID FOLDER-Bit \_ in **PR_VALID_FOLDER_MASK.** 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Öffnen Sie den Ordner, in dem alle eingehenden Nachrichten einer bestimmten Klasse platziert werden
  
1. Rufen [Sie IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner abzurufen, und setzen Sie den  _lpszMessageClass-Parameter_ so, dass er auf eine Zeichenzeichenfolge verweisen soll, die die Nachrichtenklasse identifiziert. Wenn Sie beispielsweise den Posteingang für Ihre IPM-Unterstruktur öffnen möchten, zeigen Sie  _lpszMessageClass auf_ IPM. Wenn Sie den Empfangsordner für IPC-Nachrichten öffnen möchten, legen Sie ihn auf IPC an. 

   Wenn kein registrierter Empfangsordner für die Nachrichtenklasse vorkommt, wählt **GetReceiveFolder** den Empfangsordner aus, dessen zugeordnete Nachrichtenklasse dem längsten möglichen Präfix der übergebenen Nachrichtenklasse entspricht. Weitere Informationen finden Sie unter [MAPI Receive Folders](mapi-receive-folders.md). 
   
   Beachten Sie, **dass PR_IPM_OUTBOX_ENTRYID-Eigenschaft** verwendet wird, um den Ordner "Outbox" nur für IPM-Nachrichten zu öffnen. Wenn Sie den Posteingang für IPC-Nachrichten öffnen, verwenden Sie stattdessen die Eintrags-ID für den Empfangsordner. Sowohl eingehende als auch ausgehende IPC-Nachrichten werden im Empfangsordner platziert. 
    
2. Rufen Sie eine von vier **OpenEntry-Methoden** auf, um den Ordner zu öffnen und einen Schnittstellenzeiger zurück, mit dem Sie darauf zugreifen können. Sie können eine der folgenden Methoden zum Öffnen eines Ordners aufrufen: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   Die bestimmte Methode, die Sie auswählen, hängt vom ordner ab, der geöffnet werden soll, und von den Objekten, die zurzeit verfügbar sind. Da die **IMAPISession-Methode** einen beliebigen Ordner für jeden Nachrichtenspeicher im aktuellen Profil öffnen kann, rufen Sie **diesen OpenEntry** auf, wenn Sie nichts über den zu öffnenden Ordner wissen. Wenn Sie wissen, welcher Nachrichtenspeicher der Ordner ist und Sie über einen Zeiger auf den Nachrichtenspeicher verfügen, rufen Sie **IMsgStore::OpenEntry auf.** 
    
   Verwenden Sie beispielsweise die **IMsgStore-Methode,** um einen Empfangsordner zu öffnen. Wenn Sie über einen Zeiger auf das Anmeldeobjekt des Nachrichtenspeicheranbieters verfügen, rufen Sie **IMSLogon::OpenEntry auf.** Da diese Anrufe direkt an den Nachrichtenspeicheranbieter und nicht über MAPI gehen, ist die Verarbeitung schneller. Wenn der geöffnete Ordner ein Unterordner eines Ordners ist, den Sie bereits geöffnet haben, rufen Sie die **IMAPIContainer::OpenEntry-Methode** des geöffneten Ordners auf. Die **IMAPIContainer-Methode** öffnet nur Unterordner eines aktuell geöffneten Ordners und ist die einzige Methode, die garantiert mit kurzfristigen Eintragsbezeichnern funktioniert. 
    
3. Wenn Sie Änderungen am zu öffnenden Ordner vornehmen möchten, geben Sie eine Zugriffsebene an, indem Sie entweder das FLAG MAPI BEST ACCESS oder MAPI MODIFY im \_ \_ \_ **OpenEntry-Aufruf** festlegen. Diese Flags sind Vorschläge an den Nachrichtenspeicheranbieter, um beim Öffnen des Ordners die höchste Zugriffsebene für MAPI BEST ACCESS oder Lese-/Schreibzugriff für MAPI MODIFY zu \_ \_ \_ gewähren. 

   Da es sich bei diesen Kennzeichen nur um Vorschläge handelt, kann der Ordner mit der von Ihnen erwarteten Zugriffsebene geöffnet werden. Durch Abrufen der **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) -Eigenschaft können Sie den Bereich der Vorgänge bestimmen, die für den geöffneten Ordner ausgeführt werden können. 
    
   Da viele Nachrichtenspeicheranbieter den Wert für diese Eigenschaft bei Bedarf berechnen, anstatt sie als Ordnereigenschaft oder als Spalte in ihrer Hierarchietabelle zu unterstützen, kann das Abrufen dieser Eigenschaft zeitaufwändig sein. Eine alternative Strategie besteht in dem Versuch, den erforderlichen Vorgang durchzuführen, und bei Bedarf einen Fehler zurück.
    
## <a name="see-also"></a>Siehe auch

- [PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

