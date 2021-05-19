---
title: Codieren von Empfängertabellen mithilfe von TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417959"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codieren von Empfängertabellen mithilfe von TNEF

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Codierung einer Empfängertabelle in den TNEF-Stream ist selten erforderlich, da die meisten Messagingsysteme Empfängerlisten direkt unterstützen. Im Allgemeinen werden die Empfängereigenschaften im Nachrichtenkopf übertragen. Wenn die Aufnahme der Empfängertabelle erforderlich ist, kann TNEF die Empfängertabelle als Teil der üblichen Verarbeitung codieren. Dies erfolgt während der ersten Phase der TNEF-Verarbeitung. Der Transportanbieter kann die Empfängertabelle der Nachricht enthalten, indem die [ITnef::AddProps-Methode](itnef-addprops.md) mit der in der Inklusionsliste angegebenen **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) -Eigenschaft aufruft. TNEF ruft die Empfängertabelle aus der Nachricht ab, fragt den Spaltensatz ab und verarbeitet jede Zeile der Tabelle in den TNEF-Stream.
  
Eine alternative Methode ist verfügbar, wenn der Transportanbieter die Empfängertabelle ändern muss, bevor sie codiert wird. Der Transportanbieter kann die erforderliche Tabelle erstellen und dann die [ITnef::EncodeRecips-Methode](itnef-encoderecips.md) aufrufen. Wenn NULL im  _lpRecipTable-Parameter_ übergeben wird, wird die Empfängertabelle wie für **ITnef::AddProps** beschrieben direkt aus der Nachricht übernommen.
  

