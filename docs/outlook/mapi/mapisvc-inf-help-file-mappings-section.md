---
title: MapiSvc.inf [Help File Mappings] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407557"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc.inf [Help File Mappings] Section

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der **Abschnitt [Hilfedateizuordnungen]** enthält Einträge, die jeweils einen Nachrichtendienst der Datei zuordnen, die Hilfe für vom Dienst generierte Fehler bietet. Einträge in diesem Abschnitt verwenden das folgende Format: 
  
 **[Hilfedateizuordnungen]** _Name der Hilfedatei_ des  =   _Nachrichtendiensts_
  
Der Name des Nachrichtendiensts ist der Name des installierten Nachrichtendiensts. Der Name der Hilfedatei ist der Name der Datei, in der sich die Fehlerinformationen befinden. Das folgende Beispiel zeigt einen typischen **Abschnitt [Hilfedateizuordnungen],** der Einträge für drei Dienste enthält: MAPI, der MsgService-Dienst und der MS-Dienst. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


