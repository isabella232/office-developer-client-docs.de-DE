---
title: Implementieren der IClassFactory-Schnittstelle für Formularserver
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388049"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementieren der IClassFactory-Schnittstelle für Formularserver

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) ist die OLE-Schnittstelle, die Clientanwendungen zum Erstellen neuer Formularobjekte der Nachrichtenklasse des Formulars Servers verwenden. Die folgende Tabelle enthält die **IClassFactory** -Methoden, die erforderlich sind. 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Erstellt ein neues Formularobjekt.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Sperrt den Formular-Server im Arbeitsspeicher an, sodass Startup Aufwand vermieden werden kann, wenn mehrere Formularobjekte erstellt werden.  <br/> |
   
Für alle erforderlichen Informationen zum Implementieren dieser Methods finden Sie unter den Abschnitt COM und ActiveX-Objekt Services im Windows SDK.
  
## <a name="see-also"></a>Siehe auch



[Schreiben von Formularservercode](writing-form-server-code.md)

