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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329631"
---
# <a name="using-the-mapi-utilities"></a>Verwenden der MAPI-Dienstprogramme

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI-Dienstprogramme bestehen aus Tabellendaten und Eigenschaftendaten Objekten sowie verschiedenen Funktionen zur Unterstützung verschiedener Features. Ein Client kann nur diese Dienstprogramme benötigen und sich nicht beim MAPI-Subsystem anmelden, um eine Verbindung mit Dienstanbietern herzustellen. Wenn Ihr Client in diese Kategorie passt, rufen Sie die API-Funktion [ScInitMapiUtil](scinitmapiutil.md) anstelle der [MAPIInitialize](mapiinitialize.md) -Funktion bei der Initialisierungszeit. 
  
 **ScInitMapiUtil** ermöglicht Clients das Verwenden von Hilfsfunktionen, die MAPI-Zuweisungen erfordern, die jedoch nicht explizit nach den Zuordnungen Fragen. Wenn es Zeit zum Herunterfahren ist, rufen Sie [DeinitMapiUtil](deinitmapiutil.md) auf, um Ressourcen anstelle von [MAPIUninitialize](mapiuninitialize.md)zu erhalten. Clients, die **MAPIInitialize** nie aufrufen, sollten **MAPIUninitialize**aufrufen.
  
Wenn Sie **ScInitMapiUtil** statt **MAPIInitialize** aufgerufen haben und Tabellen über die **ITableData** -Methoden statt über die **IMAPITable** -Methoden verwenden, beachten Sie, dass Tabellen Benachrichtigungen nicht funktionieren. Benachrichtigungen erfordern die Verwendung der MAPI-Bibliotheken und [IMAPITable: IUnknown](imapitableiunknown.md).
  

