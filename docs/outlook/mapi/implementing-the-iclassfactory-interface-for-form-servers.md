---
title: Implementieren der IClassFactory-Schnittstelle für Formular-Servern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792575"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementieren der IClassFactory-Schnittstelle für Formular-Servern

  
  
**Betrifft**: Outlook 
  
[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) ist die OLE-Schnittstelle, die Clientanwendungen zum Erstellen neuer Formularobjekte der Nachrichtenklasse des Formulars Servers verwenden. Die folgende Tabelle enthält die **IClassFactory** -Methoden, die erforderlich sind. 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|[CreateInstance](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |Erstellt ein neues Formularobjekt.  <br/> |
|[LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |Sperrt den Formular-Server im Arbeitsspeicher an, sodass Startup Aufwand vermieden werden kann, wenn mehrere Formularobjekte erstellt werden.  <br/> |
   
Für alle erforderlichen Informationen zum Implementieren dieser Methods finden Sie unter den Abschnitt COM und ActiveX-Objekt Services im Windows SDK.
  
## <a name="see-also"></a>Siehe auch



[Schreiben von Formularcode Server](writing-form-server-code.md)

