---
title: MAPI-Sitzungs Verarbeitung
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
# <a name="mapi-session-handling"></a>MAPI-Sitzungs Verarbeitung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bevor Sie mit Dienstanbietern und einem zugrunde liegenden Messagingsystem kommunizieren können, müssen Sie eine Sitzung erstellen. Eine MAPI-Sitzung ist ein Link von einem Client zu anderen MAPI-Komponenten. Als Ergebnis des erfolgreichen Startens einer Sitzung gibt MAPI an Clients einen Zeiger auf ein Session-Objekt zurück, ein Objekt, das die **IMAPISession** -Schnittstelle implementiert. Weitere Informationen finden Sie unter [IMAPISession: IUnknown](imapisessioniunknown.md). Sie können die Methoden der **IMAPISession** -Schnittstelle verwenden, um auf die Objekte von Adressbuch-und Nachrichtenspeicher Anbietern zuzugreifen, auf mehrere Tabellen zuzugreifen, Formulare anzuzeigen, Transportanbieter Eigenschaften festzulegen und die Verwaltung von Profil-und Nachrichtendiensten durchzuführen. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Starten einer MAPI-Sitzung](starting-a-mapi-session.md)
  
> Beschreibt das Starten einer MAPI-Sitzung und enthält Links zu Themen mit detaillierteren Informationen.
    
[Beenden einer MAPI-Sitzung](ending-a-mapi-session.md)
  
> Beschreibt das Beenden einer MAPI-Sitzung.
    
[Zugreifen auf Objekte mithilfe der Sitzung](accessing-objects-by-using-the-session.md)
  
> Beschreibt die Verwendung eines Sitzungs Zeigers für den Zugriff auf Sitzungsobjekte.
    
[Abrufen der primären und Anbieter Identität](retrieving-primary-and-provider-identity.md)
  
> Beschreibt die Eigenschaften, die zum Abrufen der primären und Anbieter Identität verwendet werden.
    
[Statustabelle und Statusobjekte](status-table-and-status-objects.md)
  
> Beschreibt, wie auf Informationen aus der Statustabelle zugegriffen wird.
    

