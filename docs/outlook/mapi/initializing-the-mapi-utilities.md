---
title: Initialisieren der MAPI-Dienstprogramme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7fe01c60193dda5cd9faa1e8723246475f5dd66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571633"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisieren der MAPI-Dienstprogramme

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn der einzige Teil der MAPI, den Sie verwenden müssen, die Dienstprogramme sind , die Schnittstellen und Funktionen, die in MAPIUTIL der MAPI deklariert sind. H-Headerdatei wie **IPropData** und **ITableData** – Sie müssen **MAPIInitialize** nicht für die Initialisierung aufrufen. Weitere Informationen finden Sie unter [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)und [MAPIInitialize](mapiinitialize.md). Rufen Sie stattdessen die **ScInitMapiUtil-Funktion** auf. Weitere Informationen finden Sie unter [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** ermöglicht Clientanwendungen die Verwendung von Hilfsfunktionen und -methoden, die MAPI-Zuweisungen erfordern, die jedoch nicht explizit danach gefragt werden. 
  
Rufen Sie zum Zeitpunkt des Herunterfahrens **DenitMapiUtil** auf, um Ressourcen freizugeben, die mit den Hilfsprogrammen verbunden sind. **MAPIUninitialize** nicht aufrufen. Weitere Informationen finden Sie unter [ObjekteitMapiUtil](deinitmapiutil.md) und [MAPIUninitialize](mapiuninitialize.md).
  
Beachten Sie, dass die **ITableData-Schnittstelle** keine Tabellenbenachrichtigungen für Clients unterstützt, die **ScInitMapiUtil** anstelle von **MAPIInitialize** aufgerufen haben. 
  

