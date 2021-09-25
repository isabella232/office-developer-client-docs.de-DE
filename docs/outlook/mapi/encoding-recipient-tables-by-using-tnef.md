---
title: Codieren von Empfängertabellen mithilfe von TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4cce961a4b601f433adac1b11a650165ecf71835
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621143"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codieren von Empfängertabellen mithilfe von TNEF

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Codierung einer Empfängertabelle im TNEF-Stream ist selten erforderlich, da die meisten Messagingsysteme Empfängerlisten direkt unterstützen. Im Allgemeinen werden die Empfängereigenschaften im Nachrichtenkopf übertragen. Wenn die Aufnahme der Empfängertabelle erforderlich ist, kann TNEF die Empfängertabelle als Teil der üblichen Verarbeitung codieren. Dies geschieht in der Anfangsphase der TNEF-Verarbeitung. Der Transportanbieter kann die Empfängertabelle der Nachricht einschließen, indem die [ITnef::AddProps-Methode](itnef-addprops.md) mit der in der Einschlussliste angegebenen **PR_MESSAGE_RECIPIENTS** -Eigenschaft ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) aufgerufen wird. TNEF ruft die Empfängertabelle aus der Nachricht ab, fragt den Spaltensatz ab und verarbeitet jede Zeile der Tabelle in den TNEF-Stream.
  
Eine alternative Methode ist verfügbar, wenn der Transportanbieter die Empfängertabelle ändern muss, bevor sie codiert wird. Der Transportanbieter kann die erforderliche Tabelle erstellen und dann die [ITnef::EncodeRecips-Methode](itnef-encoderecips.md) aufrufen. Wenn NULL im  _lpRecipTable-Parameter_ übergeben wird, wird die Empfängertabelle wie für **ITnef::AddProps** beschrieben direkt aus der Nachricht übernommen.
  

