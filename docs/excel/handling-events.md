---
title: Behandeln von Ereignissen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790500"
---
# <a name="handling-events"></a>Behandeln von Ereignissen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ab Excel 2010 können XLLs Ereignisse im Lebenszyklus des asynchronen Funktion verwalten soll empfangen. Die Ereignisse sind wie folgt:
  
- **CalculationEnded**: ausgelöst, wenn Excel beendet ist berechnen. Nach diesem Ereignis können Sie Ressourcen, die während der Berechnung freigeben.
    
- **CalculationCanceled**: ausgelöst, wenn der Benutzer die Berechnung unterbrochen wird. Die XLL beendet alle asynchronen Aktivitäten. Das **CalculationEnded** -Ereignis wird unmittelbar nach diesem Ereignis ausgelöst. 
    
Um diese Ereignisse behandeln, verwendet die XLL der C-API-Funktion [XlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** und **CalculationCanceled** werden während der programmgesteuerten neuberechnung nicht ausgelöst. 
  

