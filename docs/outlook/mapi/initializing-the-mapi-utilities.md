---
title: Initialisieren der MAPI-Dienstprogramme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567671"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisieren der MAPI-Dienstprogramme

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn der einzige Teil des MAPI, die Sie verwenden müssen, sind die Dienstprogramme – die Schnittstellen und Funktionen in der MAPI-MAPIUTIL deklariert. H-Headerdatei wie **IPropData** und **ITableData** – Sie müssen nicht für die Initialisierung **"MAPIInitialize"** aufrufen. Weitere Informationen finden Sie unter [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md), und ["MAPIInitialize"](mapiinitialize.md). Rufen Sie stattdessen die **ScInitMapiUtil** -Funktion. Weitere Informationen finden Sie unter [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** von Clientanwendungen Hilfsfunktionen und Methoden, die MAPI-Allocators erfordern, aber, die nicht mehr für diese explizit, verwenden. 
  
Rufen Sie beim Herunterfahren **DeinitMapiUtil** zum Freigeben von Ressourcen, die mit der Dienstprogramme verbunden ist. **MAPIUninitialize**nicht aufrufen. Weitere Informationen finden Sie unter [DeinitMapiUtil](deinitmapiutil.md) und [MAPIUninitialize](mapiuninitialize.md).
  
Beachten Sie, dass die Schnittstelle **ITableData** Tabelle Benachrichtigungen für Clients nicht unterstützt, die **ScInitMapiUtil** statt **"MAPIInitialize"** aufgerufen haben. 
  

