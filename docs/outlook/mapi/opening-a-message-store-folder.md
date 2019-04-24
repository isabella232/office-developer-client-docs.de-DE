---
title: Öffnen eines Nachrichtenspeicherordners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331374"
---
# <a name="opening-a-message-store-folder"></a>Öffnen eines Nachrichtenspeicherordners

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor ein Ordner geöffnet werden kann, muss sein Eintragsbezeichner verfügbar sein. Für die meisten Ordner ist dies das Abrufen der **PR_ENTRYID** -Eigenschaften. Für spezielle Ordner wie einige der IPM-subtree-Ordner und andere Stammordner definiert MAPI spezielle Eintrags-ID-Eigenschaften, auf die durch Aufrufen der **IMAPIProp::** GetProps-Methode des Nachrichtenspeichers zugegriffen werden kann. Diese Eintragsbezeichner sind immer langfristig und werden wie folgt benannt: 
  
|**Folder**|**Eintrags-ID-Eigenschaft**|
|:-----|:-----|
|Postausgang  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([Pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md)) (Nur IPM-Nachrichtenklasse)  <br/> |
|Ordner "Gelöschte Elemente"  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([Pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|Ordner 'Gesendete Elemente'  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([Pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM-Stammordner  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([Pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|Suchergebnisse Stammordner  <br/> |**PR_FINDER_ENTRYID** ([Pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md))  <br/> |
|Stammordner allgemeine Ansichten  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([Pidtagcommonviewsentryid (](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Stammordner persönliche Ansichten  <br/> |**PR_VIEWS_ENTRYID** ([Pidtagviewsentryid (](pidtagviewsentryid-canonical-property.md))  <br/> |
|Kontakte Stammordner  <br/> |**PR_IPM_CONTACT_ENTRYID** ([Pidtagipmcontactentryid (](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Entwurfs Stammordner  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([Pidtagipmdraftsentryid (](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Journal Stammordner  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([Pidtagipmjournalentryid (](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Kalender Stammordner  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([Pidtagipmappointmententryid (](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Notes-Stammordner  <br/> |**PR_IPM_NOTE_ENTRYID** ([Pidtagipmnoteentryid (](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Aufgaben Stammordner  <br/> |**PR_IPM_TASK_ENTRYID** ([Pidtagipmtaskentryid (](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Bevor Sie versuchen, einen dieser speziellen Eintragsbezeichner abzurufen, rufen Sie **die\_PR VALID_FOLDER_MASK** ([pidtagvalidfoldermask (](pidtagvalidfoldermask-canonical-property.md))-Eigenschaft des Nachrichtenspeichers ab. **PR\_VALID_FOLDER_MASK** ist eine Bitmaske, die identifiziert, welche der speziellen Eintragsbezeichner vorhanden sind. Für jeden speziellen Ordner gibt es ein Bit. Wenn das Bit festgelegt ist, wird angegeben, dass der entsprechende Ordner unterstützt wird und einen gültigen Eintragsbezeichner aufweist. Wenn beispielsweise der Ordner "Gelöschte Elemente" vorhanden ist und eine gültige Eintrags-ID\_aufweist, wird das IPM_WASTEBASKET_VALID-Bit des Ordners in **PR_VALID_FOLDER_MASK**festgelegt. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Öffnen Sie den Ordner, in dem alle eingehenden Nachrichten einer bestimmten Klasse abgelegt werden.
  
1. Rufen Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) auf, um den Eintragsbezeichner abzurufen, und legen Sie den _lpszMessageClass_ -Parameter so fest, dass er auf eine Zeichenfolge zeigt, die die Nachrichtenklasse identifiziert. Wenn Sie beispielsweise den Posteingang für Ihre IPM-Unterstruktur öffnen möchten, zeigen Sie _lpszMessageClass_ auf IPM. Wenn Sie den Empfangsordner für IPC-Nachrichten öffnen möchten, legen Sie ihn so fest, dass er auf IPC zeigt. 

   Wenn kein registrierter Empfangsordner für die Nachrichtenklasse vorhanden ist, wählt **GetReceiveFolder** den Ordner Receive aus, dessen zugeordnete Nachrichtenklasse mit dem längsten möglichen Präfix der übergebenen Nachrichtenklasse übereinstimmt. Weitere Informationen finden Sie unter [MAPI-Empfangsordner](mapi-receive-folders.md). 
   
   Beachten Sie, dass die **PR_IPM_OUTBOX_ENTRYID** -Eigenschaft verwendet wird, um den Ordner Postausgang nur für IPM-Nachrichten zu öffnen. Wenn Sie den Postausgang für IPC-Nachrichten öffnen, verwenden Sie stattdessen die Eintrags-ID für den zugehörigen Empfänger Ordner. Sowohl eingehende als auch ausgehende IPC-Nachrichten werden im Empfangsordner gespeichert. 
    
2. Rufen Sie eine der **** vier OpenEntry-Methoden auf, um den Ordner zu öffnen und einen Schnittstellenzeiger zurückzugeben, den Sie für den Zugriff verwenden können. Sie können eine der folgenden Methoden aufrufen, um einen Ordner zu öffnen: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   Die ausgewählte Methode hängt vom zu öffnenden Ordner und den zu diesem Zeitpunkt verfügbaren Objekten ab. Da die **IMAPISession** -Methode einen beliebigen Ordner für einen beliebigen Nachrichtenspeicher im aktuellen Profil öffnen kann, rufen Sie diesen OpenEntry- **Eintrag** auf, wenn Sie nichts über den zu öffnenden Ordner wissen. Wenn Sie wissen, welcher Nachrichtenspeicher den Ordner besitzt und Sie über einen Zeiger auf den Nachrichtenspeicher verfügen, rufen Sie **IMsgStore:: OpenEntry**auf. 
    
   Verwenden Sie beispielsweise die **IMsgStore** -Methode, um einen Empfangsordner zu öffnen. Wenn Sie über einen Zeiger auf das Logon-Objekt des Nachrichtenspeicher Anbieters verfügen, rufen Sie **IMSLogon:: OpenEntry**auf. Da diese Aufrufe direkt an den Nachrichtenspeicher Anbieter statt über MAPI geleitet werden, erfolgt die Verarbeitung schneller. Wenn der Ordner, den Sie öffnen, ein Unterordner eines Ordners ist, den Sie bereits geöffnet haben, rufen Sie die **IMAPIContainer:: OpenEntry** -Methode des geöffneten Ordners auf. Die **IMAPIContainer** -Methode öffnet nur Unterordner eines derzeit geöffneten Ordners und ist die einzige Methode, die für die Arbeit mit kurzfristigen Eintrags Bezeichnern garantiert ist. 
    
3. Wenn Sie Änderungen am zu öffnenden Ordner vornehmen möchten, geben Sie eine Zugriffsebene an, indem Sie im openEntry-Aufruf\_entweder\_die MAPI-\_Option "Bester Zugriff **** " oder "MAPI ändern" festlegen. Diese Flags sind Vorschläge für den Nachrichtenspeicher Anbieter, die beim Öffnen des Ordners die höchste Zugriffsebene\_,\_für den besten MAPI-Zugriff oder Lese-/Schreibzugriff\_für MAPI-Änderungen gewähren. 

   Da diese Flags nur Vorschläge sind, kann der Ordner mit der erwarteten Zugriffsebene nicht geöffnet werden. Durch Abrufen der **PR_ACCESS** ([pidtagaccess (](pidtagaccess-canonical-property.md))-Eigenschaft können Sie den Bereich der Vorgänge bestimmen, die für den geöffneten Ordner ausgeführt werden können. 
    
   Da jedoch viele Nachrichtenspeicher Anbieter den Wert für diese Eigenschaft bei Bedarf berechnen, statt sie als Ordnereigenschaft oder als Spalte in ihrer Hierarchietabelle zu unterstützen, kann das Abrufen von zeitaufwändig sein. Eine alternative Strategie besteht darin, den Vorgang auszuführen, den Sie ausführen müssen, und bei Bedarf einen Fehler zurückzugeben.
    
## <a name="see-also"></a>Siehe auch

- [Kanonische PidTagEntryId-Eigenschaft](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

