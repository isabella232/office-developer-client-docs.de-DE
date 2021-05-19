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
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420948"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisieren der MAPI-Dienstprogramme

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Der einzige Teil der MAPI, den Sie verwenden müssen, die Dienstprogramme sind – die Schnittstellen und Funktionen, die in MAPI's MAPIUTIL deklariert sind. H-Headerdatei wie **IPropData** und **ITableData** – Sie müssen **MAPIInitialize** nicht für die Initialisierung aufrufen. Weitere Informationen finden Sie unter [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)und [MAPIInitialize](mapiinitialize.md). Rufen Sie stattdessen die **ScInitMapiUtil-Funktion** auf. Weitere Informationen finden Sie unter [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** ermöglicht Clientanwendungen die Verwendung von Hilfsfunktionen und Methoden, die MAPI-Zuweisungen erfordern, die jedoch nicht explizit nach ihnen gefragt werden. 
  
Rufen Sie zum Zeitpunkt des Herunterfahrens **DeinitMapiUtil** auf, um mit den Dienstprogrammen verbundene Ressourcen frei zu geben. Rufen Sie **MAPIUninitialize nicht auf.** Weitere Informationen finden Sie unter [DeinitMapiUtil](deinitmapiutil.md) und [MAPIUninitialize](mapiuninitialize.md).
  
Beachten Sie, dass die **ITableData-Schnittstelle** keine Tabellenbenachrichtigungen für Clients unterstützt, die **ScInitMapiUtil anstelle** von **MAPIInitialize aufgerufen haben.** 
  

