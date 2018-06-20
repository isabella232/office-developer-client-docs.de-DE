---
title: Überprüfen und Initialisieren eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 74f0a1fe-2a79-4b32-ab88-85a8839a2639
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48883ec33db9ffd6b3e7cc6e16ae9c2487a31607
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795847"
---
# <a name="validating-and-initializing-a-message-store"></a>Überprüfen und Initialisieren eines Nachrichtenspeichers

  
  
**Betrifft**: Outlook 
  
Beim Öffnen eines Nachrichtenspeichers über die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode ohne das MDB_NO_MAIL-Flag MAPI mehrere Ordner erstellt und ihnen Standardnamen und Rollen zuweist. MAPI ist verantwortlich für die Erstellung dieser Ordner um Inkompatibilitäten zu vermeiden, die zwangsläufig auftreten würde, wenn Clients oder Nachricht Anbieter verantwortlich für die Erstellung wurden. 
  
In einigen Fällen ist es erforderlich, um sicherzustellen, dass die entsprechenden Ordner erstellt wurden und dass sie gültig sind. Die [HrValidateIPMSubtree](hrvalidateipmsubtree.md) -Funktion ist für diesen Zweck verfügbar. Wenn Sie den standardmäßigen Nachrichtenspeicher überprüfen, übergeben Sie die Kennzeichen MAPI_FULL_IPM_TREE. Eine umfangreichere Gruppe von Ordnern wird für den standardmäßigen Nachrichtenspeicher erstellt. Wenn **HrValidateIPMSubtree** das Flag MAPI_FULL_IPM_TREE empfängt, überprüft es die folgenden Ordner: 
  
- Stammordner für die IPM-Unterstruktur
    
- Ordner Gelöschte Objekte im Stammordner IPM
    
- Ordner Posteingang im Stammordner IPM
    
- Postausgang im Stammordner IPM
    
- Ordner Gesendete Objekte im Stammordner IPM
    
- Ansichten für Ordner im Stammordner der Nachrichtenspeicher
    
- Allgemeine Ansichten im Stammordner der Nachrichtenspeicher
    
- Suchordner im Stammordner der Nachrichtenspeicher
    
Ist der Nachrichtenspeicher nicht Standard, können Sie festlegen oder das Flag MAPI_FULL_IPM_TREE nicht festgelegt. Wenn dieses Flag **HrValidateIPMSubtree** prüft, ob nur den Stammordner für die Unterstruktur nicht festgelegt ist, speichern den Ordner Gelöschte Objekte und der Stammordner für Nachricht Suchergebnisse. 
  
Um einen Nachrichtenspeicher initialisieren, speichern Sie die folgenden Eigenschaften im Arbeitsspeicher, damit sie verfügbar sind:
  
- **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))
    
- **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))
    
Diese Eigenschaften sind Bitmasken, die Features des Nachrichtenspeichers beschreiben. **PR_VALID_FOLDER_MASK** verfügt über ein Bit für jeden speziellen Ordner, der im Nachrichtenspeicher vorhanden ist und verfügt über einen Eintrag zugewiesene Bezeichner, der gültig ist festgelegt. Weitere Informationen zu den Zugriff auf diese Ordner und ihre Eintragsbezeichner finden Sie unter [Öffnen einen Speicherordner Nachricht](opening-a-message-store-folder.md). 
  
 **PR_STORE_SUPPORT_MASK** verfügt über ein Bit für jedes Feature im Nachrichtenspeicher unterstützt festgelegt. Beispielsweise wenn ein Nachrichtenspeicher Benachrichtigung und formatierten Text unterstützt, haben dessen **PR_STORE_SUPPORT_MASK** die STORE_NOTIFY_OK und STORE_RTF_OK Bits festgelegt. 
  
Andere Eigenschaften, die lokal gespeichert werden sollen enthalten den Eintrag-IDs für die Ordner, die die **PR_VALID_FOLDER_MASK** -Eigenschaft als gültig beschreibt. Jeder dieser speziellen Ordner, mit Ausnahme der Ordner Posteingang verfügt über eine Eintrags-ID-Eigenschaft zugeordnet. Beispielsweise wird die Eintrags-ID für den Ordner Postausgang seiner **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))-Eigenschaft. Da diese Ordner die Ordner, die häufig geöffnet wird sind, ist es ratsam, haben ihre Eintragsbezeichner immer leicht zugänglich sind.
  

