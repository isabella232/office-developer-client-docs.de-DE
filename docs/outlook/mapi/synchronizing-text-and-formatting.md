---
title: Synchronisieren von Text und Formatierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 40d7a45ab97e0d2f8e9d3db1e1d38eb3bdb75158
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795710"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisieren von Text und Formatierung

  
  
**Betrifft**: Outlook 
  
Die größte Herausforderung beim Senden von Nachrichten Rich Text Format (RTF) wird den Text mit der Formatierung synchronisiert halten. Um sicherzustellen, dass beim Empfang von Nachrichten an ihrem Ziel wie für ihre Ersteller für die direkte Verwendung und sind die Text und Formatierung werden synchronisiert, MAPI bietet die [RTFSync](rtfsync.md) -Funktion. **RTFSync** wird beim Download von Nachrichten mit einem Dienstanbieter Transport in der Regel durch RTF-fähigen Clients vor dem eingehende Nachrichten anzeigen und die MAPI-Warteschlange aufgerufen. Anrufer Geben Sie den Bereich der möglichen Abweichung, indem Sie ein oder zwei Flags zu **RTFSync**übergeben:
  
- RTF_SYNC_BODY_CHANGED an, dass eine Änderung im Nachrichtentext.
    
- RTF_SYNC_RTF_CHANGED an, dass eine Änderung in der Nachricht formatieren.
    
Synchronisierungsvorgangs, das in **RTFSync** auftritt, ist eine anspruchsvolle CRC-Prüfung (CRC) des Texts Nachricht, die einige Zeichen ignoriert und andere konvertiert. Zeichen, die in den meisten Fällen von Transportanbieter hinzugefügt wurden, werden ignoriert. MAPI definiert verschiedene Eigenschaften für die Arbeit mit RTF, wie in der folgenden Tabelle beschrieben. 
  
|**RTF-Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Gibt den Anfang des Nachrichtentexts.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Das Ergebnis der CRC-Prüfung von den Nachrichtentext enthält.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Enthält die Anzahl der Zeichen in **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Legen Sie TRUE, wenn die Nachricht Text und Formatierung synchronisiert wurden.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Enthält der Anzahl der Zeichen Nonwhitespace, Länderkürzel den Nachrichtentext an.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Enthält die Anzahl der Zeichen Nonwhitespace, die den Nachrichtentext aufgenommen wird.  <br/> |
   

