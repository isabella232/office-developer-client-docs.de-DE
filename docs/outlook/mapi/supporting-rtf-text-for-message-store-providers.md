---
title: Unterstützung für RTF-Text für Nachrichtenspeicher-Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795693"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Unterstützung für RTF-Text für Nachrichtenspeicher-Anbieter

  
  
**Betrifft**: Outlook 
  
Einige Clientanwendungen können Benutzer Rich Text Format (RTF) Text in ihren Nachrichten verwenden. Wenn Ihre Nachricht Anbieter muss zur Unterstützung von RTF-Text in Nachrichten gespeichert werden sollen, muss es zur Behandlung der Eigenschaft **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), zusätzlich zu den **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft. In erster Linie, bedeutet dies beide Eigenschaften speichern und dabei sicherstellen, dass **PR_BODY** eine nur-Text-Version des Texts in **PR_RTF_COMPRESSED**enthält. Die Funktion [RTFSync](rtfsync.md) eignet sich für diesen Zweck. 
  
Es gibt zwei Flags, die in der Nachricht Store-Objekt **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festgelegt werden können, die Clients mitteilen, was sie vom Anbieter für die Nachricht im Hinblick auf die **PR_BODY** und **PR_ erwarten können RTF_COMPRESSED** Nachrichten im Nachrichtenspeicher-Eigenschaften. Das STORE_RTF_OK-Flag gibt an, dass der Speicher den Wert der Eigenschaft **PR_BODY** aus der Eigenschaft **PR_RTF_COMPRESSED** dynamisch der Benutzer von der Last generieren kann des sie explizit synchronisieren entlastet. Das STORE_UNCOMPRESSED_RTF-Flag gibt an, dass die Nachricht Informationsdienst nicht komprimierte Daten in **PR_RTF_COMPRESSED**unterstützen kann.
  
Die Eigenschaft **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) zu löschen, wenn die **PR_BODY** -Eigenschaft geändert wird, um ordnungsgemäß mit Clientanwendungen interagieren, die RTF-Text unterstützen müssen Nachricht-Anbieter, die keine für RTF-Text Unterstützung . 
  
## <a name="see-also"></a>Siehe auch



[Nachrichtenspeicher-Features](message-store-features.md)

