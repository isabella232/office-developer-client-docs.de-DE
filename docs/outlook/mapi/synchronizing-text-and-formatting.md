---
title: Synchronisieren von Text und Formatierung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435103"
---
# <a name="synchronizing-text-and-formatting"></a>Synchronisieren von Text und Formatierung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die wichtigste Herausforderung beim Senden von RTF-Nachrichten (Rich Text Format) ist, dass der Text mit der Formatierung synchronisiert bleibt. Um sicherzustellen, dass Nachrichten an Ihrem Ziel ankommen, werden Sie als ihre Absender beabsichtigt, und der Text und die Formatierung werden synchronisiert, MAPI stellt die [RTFSync](rtfsync.md) -Funktion bereit. **RTFSync** wird in der Regel von RTF-fähigen Clients aufgerufen, bevor eingehende Nachrichten und der MAPI-Spooler angezeigt werden, wenn Nachrichten an einen Transportanbieter heruntergeladen werden. Anrufer geben den Bereich möglicher Diskrepanz an, indem Sie ein oder zwei Flags an **RTFSync**übergeben:
  
- RTF_SYNC_BODY_CHANGED, um eine Änderung im Nachrichtentext anzuzeigen.
    
- RTF_SYNC_RTF_CHANGED, um eine Änderung der Nachrichtenformatierung anzuzeigen.
    
Beim Synchronisierungsvorgang in **RTFSync** handelt es sich um eine ausgeklügelte zyklische Redundanzprüfung des Nachrichtentexts, der einige Zeichen ignoriert und andere konvertiert. Zeichen, die von Transportanbietern höchstwahrscheinlich hinzugefügt wurden, werden ignoriert. MAPI definiert mehrere Eigenschaften für das Arbeiten mit RTF, wie in der folgenden Tabelle beschrieben. 
  
|**RTF-Eigenschaft**|**Beschreibung**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([Pidtagrtfsyncbodytag (](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Gibt den Anfang des eigentlichen Nachrichtentexts an.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([Pidtagrtfsyncbodycrc (](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Enthält das Ergebnis der Überprüfung der zyklischen Redundanz des Nachrichtentexts.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([Pidtagrtfsyncbodycount (](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Enthält die Anzahl der Zeichen in **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([Pidtagrtfinsync (](pidtagrtfinsync-canonical-property.md))  <br/> |Wird auf TRUE festgelegt, wenn der Nachrichtentext und die Formatierung synchronisiert wurden.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([Pidtagrtfsyncprefixcount (](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Enthält die Anzahl von Leerzeichen, die den Nachrichtentext bevorstehen.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([Pidtagrtfsynctrailingcount (](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Enthält die Anzahl von Leerzeichen, die den Nachrichtentext nachverfolgen.  <br/> |
   

