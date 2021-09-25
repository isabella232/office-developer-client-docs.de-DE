---
title: Behandeln von Fehlern bei benannten Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6942690214af49274608a48490b8437bd59bff24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551499"
---
# <a name="handling-named-property-errors"></a>Behandeln von Fehlern bei benannten Eigenschaften
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
When a request is made to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) that is too large for the implementer to handle, the error value MAPI_E_TOO_BIG is returned. Callers must divide their request into several requests, calling the appropriate method in a loop. 
  
Wenn ein Anruf f�hrt partielle Erfolg, beispielsweise wenn die Anforderung f�r die Namen von ist, die bestimmte Bezeichner zuordnen und einen oder mehrere Namen gefunden werden k�nnen, **GetNamesFromIDs** MAPI_W_ERRORS_RETURNED zur�ckgibt und platziert PT_ERROR in den Eigenschaftstyp f�r die fehlenden Eigenschaft im Array Tag-Eigenschaft. 
  
In einigen F�llen ein Client sendet einen Anruf an **GetNamesFromIDs**, der keine Eigenschaften zur�ckgegeben werden, z. B., wenn es sind keine Eigenschaften in einem angegebenen Eigenschaftensatz oder alle benannte Eigenschaften eines Typs werden durch die Kennzeichen ausgeschlossen werden. Clients k�nnen Dienstanbieter zu erwarten: 
  
- Geben Sie S_OK zur�ck.
    
- Legen Sie den Inhalt der Eigenschaft Tag Array Zeiger in ein Array der neu zugeordnete Eigenschaft Tag mit seinem **cValues** Mitglied auf 0 (null) festgelegt. 
    
- Set the contents of the [MAPINAMEID](mapinameid.md) structure array to NULL. 
    
- Legen Sie den Inhalt der Anzahl **MAPINAMEID** Strukturen auf 0 (null). 
    
## <a name="see-also"></a>Siehe auch

- [Benannte Eigenschaften MAPI](mapi-named-properties.md)

