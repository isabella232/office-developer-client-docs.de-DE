---
title: MAPI-Sitzungsbehandlung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422061"
---
# <a name="mapi-session-handling"></a>MAPI-Sitzungsbehandlung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie mit Dienstanbietern und einem zugrunde liegenden Messagingsystem kommunizieren können, müssen Sie eine Sitzung einrichten. Eine MAPI-Sitzung ist ein Link von einem Client zu anderen MAPI-Komponenten. Als Ergebnis des erfolgreichen Startens einer Sitzung gibt MAPI an Clients einen Zeiger auf ein Sitzungsobjekt zurück – ein Objekt, das die **IMAPISession-Schnittstelle** implementiert. Weitere Informationen finden Sie unter [IMAPISession : IUnknown](imapisessioniunknown.md). Mit den Methoden der **IMAPISession-Schnittstelle** können Sie auf die Objekte von Adressbuch- und Nachrichtenspeicheranbietern zugreifen, auf mehrere Tabellen zugreifen, Formulare anzeigen, Eigenschaften des Transportanbieters festlegen und die Profil- und Nachrichtendienstverwaltung durchführen. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Starten einer MAPI-Sitzung](starting-a-mapi-session.md)
  
> Beschreibt das Starten einer MAPI-Sitzung und enthält Links zu Themen mit ausführlicheren Informationen.
    
[Beenden einer MAPI-Sitzung](ending-a-mapi-session.md)
  
> Beschreibt das Beenden einer MAPI-Sitzung.
    
[Zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md)
  
> Beschreibt die Verwendung eines Sitzungszeigers für den Zugriff auf Sitzungsobjekte.
    
[Abrufen der primären und Anbieteridentität](retrieving-primary-and-provider-identity.md)
  
> Beschreibt die Eigenschaften, die zum Abrufen der primären identität und der Anbieteridentität verwendet werden.
    
[Statustabelle und Statusobjekte](status-table-and-status-objects.md)
  
> Beschreibt den Zugriff auf Informationen aus der Statustabelle.
    

