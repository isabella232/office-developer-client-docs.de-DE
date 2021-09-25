---
title: Verwenden der MAPI-Dienstprogramme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c2ac40be8e0928e92e2f483c236f42ae8a0ee9c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566220"
---
# <a name="using-the-mapi-utilities"></a>Verwenden der MAPI-Dienstprogramme

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Dienstprogramme bestehen aus Tabellendaten- und Eigenschaftsdatenobjekten sowie einer Vielzahl von Funktionen zur Unterstützung verschiedener Features. Es ist möglich, dass ein Client nur diese Hilfsprogramme benötigt und sich nicht beim MAPI-Subsystem anmelden muss, um eine Verbindung mit Dienstanbietern herzustellen. Wenn Ihr Client in diese Kategorie passt, rufen Sie die API-Funktion [ScInitMapiUtil](scinitmapiutil.md) anstelle der [MAPIInitialize-Funktion](mapiinitialize.md) zur Initialisierungszeit auf. 
  
 **ScInitMapiUtil** ermöglicht Clients die Verwendung von Hilfsfunktionen, die MAPI-Verteiler erfordern, die jedoch nicht explizit nach den Zuteilen gefragt werden. Wenn es an der Zeit ist, herunterzufahren, rufen [Sie DenitMapiUtil](deinitmapiutil.md) auf, um Ressourcen freizugeben, anstatt [MAPIUninitialize](mapiuninitialize.md). Clients, die **MAPIInitialize** nie aufrufen, sollten **MAPIUninitialize** nicht aufrufen.
  
Wenn Sie **ScInitMapiUtil** anstelle von **MAPIInitialize** aufgerufen haben und Tabellen über die **ITableData-Methoden** statt über die **IMAPITable-Methoden** verwenden, beachten Sie, dass Tabellenbenachrichtigungen nicht funktionieren. Benachrichtigungen erfordern die Verwendung der MAPI-Bibliotheken und [IMAPITable : IUnknown](imapitableiunknown.md).
  

