---
title: Implementieren der IClassFactory-Schnittstelle für Formularserver
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5532cfc248d170952b45ba5a449f2e81a443f705
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551254"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementieren der IClassFactory-Schnittstelle für Formularserver

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) ist die OLE-Schnittstelle, mit der Clientanwendungen neue Formularobjekte der Nachrichtenklasse des Formularservers erstellen. In der folgenden Tabelle sind die erforderlichen **IClassFactory-Methoden** aufgeführt. 
  
|**Methode**|**Beschreibung**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Erstellt ein neues Formularobjekt.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Sperrt den Formularserver im Arbeitsspeicher, sodass der Startaufwand vermieden werden kann, wenn mehrere Formularobjekte erstellt werden.  <br/> |
   
Alle zum Implementieren dieser Methoden erforderlichen Informationen finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK.
  
## <a name="see-also"></a>Siehe auch



[Schreiben von Formularservercode](writing-form-server-code.md)

