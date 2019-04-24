---
title: ÜberPrüfen und Initialisieren eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 77b3f707fc36a868de5acd7c7ba4642a1da4e3c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329582"
---
# <a name="validating-and-initializing-a-message-store"></a>ÜberPrüfen und Initialisieren eines Nachrichtenspeichers

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie einen Nachrichtenspeicher über die [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) -Methode öffnen, ohne das MDB_NO_MAIL-Flag festzulegen, erstellt MAPI mehrere Ordner und weist Ihnen Standardnamen und Rollen zu. MAPI ist für die Erstellung dieser Ordner verantwortlich, um die Unverträglichkeiten zu vermeiden, die unvermeidlich wären, wenn entweder Clients oder Nachrichtenspeicher Anbieter für die Erstellung verantwortlich waren. 
  
Manchmal muss überprüft werden, ob die entsprechenden Ordner erstellt wurden und dass Sie gültig sind. Die [HrValidateIPMSubtree](hrvalidateipmsubtree.md) -Funktion steht zu diesem Zweck zur Verfügung. Wenn Sie den Standardnachrichtenspeicher überprüfen, führen Sie das MAPI_FULL_IPM_TREE-Flag aus. Eine umfangreichere Gruppe von Ordnern wird für den Standardnachrichtenspeicher erstellt. Wenn **HrValidateIPMSubtree** das MAPI_FULL_IPM_TREE-Flag erhält, prüft es die folgenden Ordner: 
  
- Stammordner für die IPM-Unterstruktur
    
- Ordner "Gelöschte Elemente" im IPM-Stammordner
    
- PostEingangsordner im IPM-Stammordner
    
- Ausgangsordner im IPM-Stammordner
    
- Ordner "Gesendete Elemente" im IPM-Stammordner
    
- Ordneransichten im Stammordner des Nachrichtenspeichers
    
- Allgemeine Ansichten im Stammordner des Nachrichtenspeichers
    
- Suchordner im Stammordner des Nachrichtenspeichers
    
Wenn der Nachrichtenspeicher nicht der Standardwert ist, können Sie das MAPI_FULL_IPM_TREE-Flag festlegen oder nicht festlegen. Wenn dieses Flag nicht festgelegt ist, sucht **HrValidateIPMSubtree** nur nach dem Stammordner für die Unterstruktur, dem Ordner "Gelöschte Elemente" und dem Stammordner für die Suchergebnisse des Nachrichtenspeichers. 
  
Um einen Nachrichtenspeicher zu initialisieren, speichern Sie die folgenden Eigenschaften im Arbeitsspeicher, damit Sie sofort verfügbar sind:
  
- **PR_VALID_FOLDER_MASK** ([Pidtagvalidfoldermask (](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Diese Eigenschaften sind Bitmasken, die Features des Nachrichtenspeichers beschreiben. **PR_VALID_FOLDER_MASK** hat ein Bit für jeden speziellen Ordner festgelegt, der im Nachrichtenspeicher vorhanden ist und einen gültigen Eintragsbezeichner besitzt. Weitere Informationen zum Zugriff auf diese Ordner und ihre Eintragsbezeichner finden Sie unter [Öffnen eines Nachrichtenspeicher Ordners](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** hat für jedes im Nachrichtenspeicher unterstützte Feature ein Bit festgelegt. Wenn beispielsweise ein Nachrichtenspeicher Benachrichtigungen und formatierten Text unterstützt, werden für dessen **PR_STORE_SUPPORT_MASK** die Bits STORE_NOTIFY_OK und STORE_RTF_OK festgelegt. 
  
Andere Eigenschaften, die lokal gespeichert werden sollen, sind die Eintrags-IDs für die Ordner, die von der **PR_VALID_FOLDER_MASK** -Eigenschaft als gültig beschrieben werden. Jedem dieser speziellen Ordner, mit Ausnahme des Ordners "Inbox", ist eine Eintrags-ID-Eigenschaft zugeordnet. Beispielsweise ist die Eintrags-ID für den Ordner Postausgang Ihre **PR_IPM_OUTBOX_ENTRYID** ([pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md))-Eigenschaft. Da es sich bei diesen Ordnern um die Ordner handelt, die häufig geöffnet werden, empfiehlt es sich, die Eingabe Kennungen bereitzustellen.
  

