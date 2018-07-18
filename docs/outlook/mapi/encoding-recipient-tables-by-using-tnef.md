---
title: Codieren von Empfängertabellen mit TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791637"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Codieren von Empfängertabellen mit TNEF

  
  
**Betrifft**: Outlook 
  
Die Codierung einer Tabelle Empfänger in der TNEF-Stream-Objekt ist nur selten erforderlich, da die meisten Messagingsysteme Empfängerlisten direkt unterstützen. Im Allgemeinen werden in der Kopfzeile der Nachricht die Empfängereigenschaften übertragen. Wenn die Aufnahme der Empfänger Tabelle erforderlich ist, kann TNEF die Empfänger Tabelle als Teil der normalen Verarbeitung codieren. Dies erfolgt während der Anfangsphase der TNEF-Verarbeitung. Der Adressbuchhierarchie kann durch Aufrufen der [ITnef::AddProps](itnef-addprops.md) -Methode mit der **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))-Eigenschaft, die in der Aufnahmeliste angegebenen Empfänger die Nachricht-Tabelle enthalten. TNEF Ruft die Empfänger Tabelle aus der Nachricht ab, fragt die Spalte festlegen und jede Zeile der Tabelle in die TNEF-Stream verarbeitet.
  
Eine alternative Methode ist verfügbar, wenn der Adressbuchhierarchie muss die Empfänger Tabelle zu ändern, bevor er codiert wird. Der Adressbuchhierarchie kann die notwendige Tabelle erstellen und dann die [ITnef::EncodeRecips](itnef-encoderecips.md) -Methode aufrufen. Wenn NULL in der _LpRecipTable_ -Parameter übergeben wird, wird die Empfänger Tabelle direkt aus der Nachricht übernommen, wie für **ITnef::AddProps**beschrieben.
  

