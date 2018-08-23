---
title: Verwenden der MAPI-Dienstprogramme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569533"
---
# <a name="using-the-mapi-utilities"></a>Verwenden der MAPI-Dienstprogramme

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Dienstprogramme Tabellendaten und Datenobjekte Eigenschaft sowie einer Reihe von Funktionen bestehen aus, um verschiedene Features unterstützen. Es ist möglich, damit ein Client benötigen nur diese Dienstprogramme und zur Anmeldung bei der MAPI-Subsystems herstellen eine Verbindung mit dem Dienstanbieter nicht haben. Wenn der Client in dieser Kategorie passt, rufen Sie die API-Funktion [ScInitMapiUtil](scinitmapiutil.md) statt der Funktion ["MAPIInitialize"](mapiinitialize.md) bei der Initialisierung. 
  
 **ScInitMapiUtil** können Clients Hilfsfunktionen verwenden Sie die MAPI-Allocators erfordern, aber, die nicht mehr für die Allocators explizit. Wenn heruntergefahren werden soll, rufen Sie [DeinitMapiUtil](deinitmapiutil.md) um Ressourcen freizugeben, sondern [MAPIUninitialize](mapiuninitialize.md). Clients, die nie **"MAPIInitialize anrufen"** sollte nicht **MAPIUninitialize**aufrufen.
  
Wenn Sie **ScInitMapiUtil** statt **"MAPIInitialize"** aufgerufen und Tabellen über die Methoden **ITableData** nicht über die **IMAPITable** -Methoden verwenden, beachten Sie, dass Tabelle Benachrichtigungen nicht funktioniert. Benachrichtigungen erfordern die Verwendung der MAPI-Bibliotheken und [IMAPITable: IUnknown](imapitableiunknown.md).
  

