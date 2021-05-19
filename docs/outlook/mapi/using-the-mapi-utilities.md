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
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409986"
---
# <a name="using-the-mapi-utilities"></a>Verwenden der MAPI-Dienstprogramme

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Dienstprogramme werden aus Tabellendaten- und Eigenschaftsdatenobjekten und einer Vielzahl von Funktionen zur Unterstützung verschiedener Features erstellt. Es ist möglich, dass ein Client nur diese Hilfsprogramme benötigt und sich nicht beim MAPI-Subsystem anmeldet, um eine Verbindung mit Dienstanbietern herzustellen. Wenn Ihr Client in diese Kategorie passt, rufen Sie die API-Funktion [ScInitMapiUtil](scinitmapiutil.md) und nicht die [MAPIInitialize-Funktion](mapiinitialize.md) zur Initialisierungszeit auf. 
  
 **ScInitMapiUtil** ermöglicht Clients die Verwendung von Hilfsfunktionen, die MAPI-Zuweisungen erfordern, die jedoch nicht explizit nach den Zuweisungen fragen. Wenn es zeit ist, heruntergefahren zu werden, rufen Sie [DeinitMapiUtil](deinitmapiutil.md) auf, um Ressourcen frei zu lassen, anstatt [MAPIUninitialize .](mapiuninitialize.md) Clients, die **MAPIInitialize nie aufrufen,** sollten **MAPIUninitialize nicht aufrufen.**
  
Wenn Sie **ScInitMapiUtil** anstelle von **MAPIInitialize** aufgerufen haben und Tabellen über die **ITableData-Methoden** und nicht über die **IMAPITable-Methoden** verwenden, sollten Sie beachten, dass Tabellenbenachrichtigungen nicht funktionieren. Benachrichtigungen erfordern die Verwendung der MAPI-Bibliotheken und [IMAPITable : IUnknown](imapitableiunknown.md).
  

