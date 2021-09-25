---
title: Behandeln von Ereignissen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0576687d6bb80f6fc3d5779db3625beccbfbc28c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572396"
---
# <a name="handling-events"></a>Behandeln von Ereignissen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ab Excel 2010 können XLLs Ereignisse empfangen, die zum Verwalten des Lebenszyklus asynchroner Funktionen entworfen wurden. Die Ereignisse sind wie folgt:
  
- **CalculationEnded:** Wird ausgelöst, wenn Excel die Berechnung abgeschlossen hat. Nach diesem Ereignis können Sie während der Berechnung zugeordnete Ressourcen freigeben.
    
- **CalculationCanceled:** Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht. Die XLL beendet asynchrone Aktivitäten. Unmittelbar nach diesem Ereignis wird das **CalculationEnded-Ereignis** ausgelöst. 
    
Um diese Ereignisse zu behandeln, verwendet die XLL die C-API-Funktion [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** und **CalculationCanceled** werden während der programmgesteuerten Neuberechnung nicht ausgelöst. 
  

