---
title: MAPI-Sitzung-Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793079"
---
# <a name="mapi-session-handling"></a>MAPI-Sitzung-Verarbeitung

  
  
**Betrifft**: Outlook 
  
Bevor Sie mit der Dienstanbieter und einer zugrunde liegenden messaging-System kommunizieren können, müssen Sie eine Sitzung einrichten. MAPI-Sitzung ist eine Verknüpfung von einem Client an andere MAPI-Komponenten. Als Ergebnis der erfolgreich starten einer Sitzung, MAPI gibt an die Clients einen Zeiger auf ein Sitzungsobjekt – ein Objekt, das die **IMAPISession** -Schnittstelle implementiert wird. Weitere Informationen finden Sie unter [IMAPISession: IUnknown](imapisessioniunknown.md). Die Methoden des **IMAPISession** -Schnittstelle können Sie den Zugriff auf die Objekte der Address Book und Message-Anbieter, Zugriff auf mehrere Tabellen, Anzeigen von Formularen, Transport Anbietereigenschaften festlegen und Verwalten des Diensts Benutzerprofil und Nachricht ausführen. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[MAPI-Sitzung starten](starting-a-mapi-session.md)
  
> Beschreibt, wie Sie eine MAPI-Sitzung zu starten, und enthält Links zu Themen mit Ausführlichere Informationen.
    
[Beenden einer MAPI-Sitzung](ending-a-mapi-session.md)
  
> Beschreibt, wie eine MAPI-Sitzung zu beenden.
    
[Zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md)
  
> Beschreibt, wie einen Sitzung Zeiger verwenden, um die Sitzungsobjekte zuzugreifen.
    
[Abrufen von primären und Anbieter Identität](retrieving-primary-and-provider-identity.md)
  
> Beschreibt die Eigenschaften, die zum Abrufen von primären und Identity Provider.
    
[Tabelle-Status und Status-Objekte](status-table-and-status-objects.md)
  
> Beschreibt das Zugreifen auf Informationen aus der Tabelle "Status".
    

