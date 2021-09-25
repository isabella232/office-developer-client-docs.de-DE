---
title: MAPI-Sitzungsbehandlung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 24a3c7bf89d23cddb6dda5344b01aead2ca38a3a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575505"
---
# <a name="mapi-session-handling"></a>MAPI-Sitzungsbehandlung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie mit Dienstanbietern und einem zugrunde liegenden Messagingsystem kommunizieren können, müssen Sie eine Sitzung einrichten. Eine MAPI-Sitzung ist eine Verknüpfung zwischen einem Client und anderen MAPI-Komponenten. Als Ergebnis des erfolgreichen Startens einer Sitzung gibt MAPI an Clients einen Zeiger auf ein Sitzungsobjekt zurück – ein Objekt, das die **IMAPISession-Schnittstelle** implementiert. Weitere Informationen finden Sie unter [IMAPISession : IUnknown](imapisessioniunknown.md). Sie können die Methoden der **IMAPISession-Schnittstelle** verwenden, um auf die Objekte von Adressbuch- und Nachrichtenspeicheranbietern zuzugreifen, auf mehrere Tabellen zuzugreifen, Formulare anzuzeigen, Transportanbietereigenschaften festzulegen und die Profil- und Nachrichtendienstverwaltung durchzuführen. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Starten einer MAPI-Sitzung](starting-a-mapi-session.md)
  
> Beschreibt, wie eine MAPI-Sitzung gestartet wird, und enthält Links zu Themen mit ausführlicheren Informationen.
    
[Beenden einer MAPI-Sitzung](ending-a-mapi-session.md)
  
> Beschreibt, wie eine MAPI-Sitzung beendet wird.
    
[Zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md)
  
> Beschreibt, wie ein Sitzungszeiger für den Zugriff auf Sitzungsobjekte verwendet wird.
    
[Abrufen der primären und der Anbieteridentität](retrieving-primary-and-provider-identity.md)
  
> Beschreibt die Eigenschaften, die zum Abrufen der primären und Anbieteridentität verwendet werden.
    
[StatusTabellen- und Statusobjekte](status-table-and-status-objects.md)
  
> Beschreibt, wie auf Informationen aus der Statustabelle zugegriffen wird.
    

