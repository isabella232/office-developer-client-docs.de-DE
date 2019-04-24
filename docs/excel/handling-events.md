---
title: Behandeln von Ereignissen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304039"
---
# <a name="handling-events"></a>Behandeln von Ereignissen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ab Excel 2010 können XLLs Ereignisse empfangen, die zum Verwalten des asynchronen Funktions Lebenszyklus entwickelt wurden. Die Ereignisse lauten wie folgt:
  
- **CalculationEnded**: wird ausgelöst, wenn Excel nicht mehr berechnet wird. Nach diesem Ereignis können Sie während der Berechnung zugewiesene Ressourcen freigeben.
    
- **CalculationCanceled**: wird ausgelöst, wenn der Benutzer die Berechnung unterbricht. Die XLL beendet alle asynchronen Aktivitäten. Unmittelbar nach diesem Ereignis wird das **CalculationEnded** -Ereignis ausgelöst. 
    
Zur Behandlung dieser Ereignisse verwendet die XLL die C-API-Funktion [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** und **CalculationCanceled** werden während der programmgesteuerten Neuberechnung nicht ausgelöst. 
  

