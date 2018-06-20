---
title: Abschnitt MapiSvc.inf [Services]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793154"
---
# <a name="mapisvcinf-services-section"></a>Abschnitt MapiSvc.inf [Services]

  
  
**Betrifft**: Outlook 
  
Im Abschnitt **[Services]** werden die Nachrichtendienste, die auf einem Computer installiert sind. Einträge in diesem Abschnitt verwenden Sie das folgende Format: 
  
 **[Services]**
  
 _Message-Dienst im Abschnittsname_ =  _Dienstname Nachricht_
  
Den Namen des Abschnitts Message-Dienst ist eine Zeichenfolge vom Nachrichtendienst enthält, die dieser Eintrag einen entsprechenden Abschnitt für den Dienst an anderer Stelle im mapisvc.inf definiert. Der Dienstname Nachricht ist der Name des installierten Dienstes. Der folgende Abschnitt zeigt drei Message-Dienste: das Standard-Adressbuch, meine eigenen Service und den Informationsspeicher-Dienst. Diese Dienste sind nur zur Veranschaulichung fiktiv. Jede Nachricht Service Implementierer würde durch den entsprechenden Eintrag für seine Messagingdiensts in diesem Abschnitt ersetzen.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Jeder Eintrag in diesem Abschnitt hat einen entsprechenden Abschnitt eigene, in dem Informationen für den Dienst gespeichert ist. Beispielsweise wird im entsprechende Abschnitt für das Standard-Adressbuch [AB] aufgerufen.
  

