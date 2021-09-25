---
title: Abschnitt "MapiSvc.inf [Help File Mappings]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2192421ddcde6771fa0eb342fc07aa28a65ddc51
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575442"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Abschnitt "MapiSvc.inf [Help File Mappings]

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Abschnitt **[Hilfedateizuordnungen]** enthält Einträge, die jeweils einen Nachrichtendienst der Datei zuordnen, die Hilfe für vom Dienst generierte Fehler bereitstellt. Die Einträge in diesem Abschnitt verwenden das folgende Format: 
  
 **[Hilfedateizuordnungen]** _Name der Hilfedatei des Nachrichtendiensts_  =   
  
Der Name des Nachrichtendiensts ist der Name des installierten Nachrichtendiensts. Der Name der Hilfedatei ist der Name der Datei, in der sich die Fehlerinformationen befinden. Das folgende Beispiel zeigt einen typischen Abschnitt **[Hilfedateizuordnungen],** der Einträge für drei Dienste enthält: MAPI, den MsgService-Dienst und den MS-Dienst. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


