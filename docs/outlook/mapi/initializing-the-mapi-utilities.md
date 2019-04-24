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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317220"
---
# <a name="initializing-the-mapi-utilities"></a>Initialisieren der MAPI-Dienstprogramme

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn der einzige Teil von MAPI, den Sie verwenden müssen, die Dienstprogramme ist – die Schnittstellen und Funktionen, die in MAPIs MAPIUTIL deklariert werden. H-Headerdatei wie **IPropData** und **ITableData** – Sie müssen **MAPIInitialize** nicht für die Initialisierung aufrufen. Weitere Informationen finden Sie unter [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)und [MAPIInitialize](mapiinitialize.md). Rufen Sie stattdessen die **ScInitMapiUtil** -Funktion auf. Weitere Informationen finden Sie unter [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** ermöglicht Clientanwendungen das Verwenden von Hilfsfunktionen und Methoden, die MAPI-Zuweisungen erfordern, die Sie jedoch nicht explizit anfordern. 
  
Rufen Sie zum Zeitpunkt des Herunterfahrens den **DeinitMapiUtil** auf, um Ressourcen für die Dienstprogramme freizugeben. Rufen Sie **MAPIUninitialize**nicht auf. Weitere Informationen finden Sie unter [DeinitMapiUtil](deinitmapiutil.md) und [MAPIUninitialize](mapiuninitialize.md).
  
Beachten Sie, dass die **ITableData** -Schnittstelle Tabellen Benachrichtigungen für Clients, die **ScInitMapiUtil** aufgerufen haben, nicht **MAPIInitialize**unterstützt. 
  

