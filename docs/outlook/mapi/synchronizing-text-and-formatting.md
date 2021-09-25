---
title: Synchronisieren von Text und Formatierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4e2d3c98124f626616b73c9180bdec721a00ba2b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624069"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisieren von Text und Formatierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die größte Herausforderung beim Senden von RTF-Nachrichten (Rich Text Format) besteht darin, den Text mit der Formatierung zu synchronisieren. Um sicherzustellen, dass Nachrichten, die am Ziel eintreffen, so sind, wie sie von den Absendern beabsichtigt sind und dass Text und Formatierung synchronisiert werden, stellt MAPI die [RTFSync-Funktion](rtfsync.md) bereit. **RTFSync** wird in der Regel von RTF-fähigen Clients aufgerufen, bevor eingehende Nachrichten angezeigt werden, und vom MAPI-Spooler, wenn Nachrichten an einen Transportanbieter heruntergeladen werden. Anrufer geben den Bereich möglicher Abweichungen an, indem sie ein oder zwei Flags an **RTFSync** übergeben:
  
- RTF_SYNC_BODY_CHANGED, um eine Änderung im Nachrichtentext anzugeben.
    
- RTF_SYNC_RTF_CHANGED, um eine Änderung der Nachrichtenformatierung anzugeben.
    
Der in **RTFSync** ausgeführte Synchronisierungsprozess ist eine anspruchsvolle cyclische Redundanzprüfung (cyclic Redundancy Check, CRC) des Nachrichtentexts, die einige Zeichen ignoriert und andere konvertiert. Zeichen, die höchstwahrscheinlich von Transportanbietern hinzugefügt wurden, werden ignoriert. MAPI definiert verschiedene Eigenschaften für die Arbeit mit RTF, wie in der folgenden Tabelle beschrieben. 
  
|**RTF-Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Gibt den Anfang des echten Nachrichtentexts an.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Enthält das Ergebnis der cyclischen Redundanzüberprüfung des Nachrichtentexts.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Enthält die Anzahl der Zeichen in **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Auf TRUE festgelegt, wenn der Nachrichtentext und die Formatierung synchronisiert wurden.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Enthält die Anzahl von Nicht-Whitespace-Zeichen, die dem Nachrichtentext vorangestellt sind.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Enthält die Anzahl der Nicht-Whitespace-Zeichen, die den Nachrichtentext nachzeichnen.  <br/> |
   

