---
title: Behandeln von Ereignissen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790500"
---
# <a name="handling-events"></a><span data-ttu-id="3dc0c-103">Behandeln von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="3dc0c-103">Handling Events</span></span>

 <span data-ttu-id="3dc0c-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3dc0c-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3dc0c-105">Ab Excel 2010 können XLLs Ereignisse im Lebenszyklus des asynchronen Funktion verwalten soll empfangen.</span><span class="sxs-lookup"><span data-stu-id="3dc0c-105">Starting in Excel 2010, XLLs can receive events designed to manage the asynchronous function life cycle.</span></span> <span data-ttu-id="3dc0c-106">Die Ereignisse sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3dc0c-106">The events are as follows:</span></span>
  
- <span data-ttu-id="3dc0c-107">**CalculationEnded**: ausgelöst, wenn Excel beendet ist berechnen.</span><span class="sxs-lookup"><span data-stu-id="3dc0c-107">**CalculationEnded**: Raised when Excel is finished calculating.</span></span> <span data-ttu-id="3dc0c-108">Nach diesem Ereignis können Sie Ressourcen, die während der Berechnung freigeben.</span><span class="sxs-lookup"><span data-stu-id="3dc0c-108">After this event, you can free resources allocated during the calculation.</span></span>
    
- <span data-ttu-id="3dc0c-109">**CalculationCanceled**: ausgelöst, wenn der Benutzer die Berechnung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="3dc0c-109">**CalculationCanceled**: Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="3dc0c-110">Die XLL beendet alle asynchronen Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="3dc0c-110">The XLL stops any asynchronous activities.</span></span> <span data-ttu-id="3dc0c-111">Das **CalculationEnded** -Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3dc0c-111">Immediately following this event, the **CalculationEnded** event is raised.</span></span> 
    
<span data-ttu-id="3dc0c-112">Um diese Ereignisse behandeln, verwendet die XLL der C-API-Funktion [XlEventRegister](xleventregister.md).</span><span class="sxs-lookup"><span data-stu-id="3dc0c-112">To handle these events, the XLL uses the C API function [xlEventRegister](xleventregister.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3dc0c-113">**CalculationEnded** und **CalculationCanceled** werden während der programmgesteuerten neuberechnung nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3dc0c-113">**CalculationEnded** and **CalculationCanceled** are not raised during programmatic recalculation.</span></span> 
  

