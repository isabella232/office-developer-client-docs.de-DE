---
title: Signalton-Makroaktion (Access PC-Datenbank-Referenz)
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 284be6222d0b81e48a061afd1d87dd32c3985feb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867580"
---
# <a name="beep-macro-action"></a><span data-ttu-id="26524-102">Signalton-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="26524-102">Beep Macro Action</span></span>


<span data-ttu-id="26524-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26524-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26524-104">Sie können die **Signalton** -Aktion verwenden, um einen Signalton über den Lautsprecher des Computers auszugeben.</span><span class="sxs-lookup"><span data-stu-id="26524-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="26524-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="26524-105">Setting</span></span>

<span data-ttu-id="26524-106">Die **Signalton** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="26524-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="26524-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26524-107">Remarks</span></span>

<span data-ttu-id="26524-108">Sie können die **Signalton** -Aktion verwenden, um auf folgende Begebenheiten hinzuweisen:</span><span class="sxs-lookup"><span data-stu-id="26524-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="26524-109">Wichtige Bildschirmänderungen sind aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="26524-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="26524-p101">Es wurden die falsche Arten von Daten in ein Steuerelement eingegeben. Beispielsweise hat der Benutzer numerische Daten in ein Textfeld-Steuerelement eingegeben.</span><span class="sxs-lookup"><span data-stu-id="26524-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="26524-112">Ein Makro hat einen angegebenen Punkt erreicht oder seine Aktionen abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="26524-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="26524-113">Häufigkeit und Dauer des Signaltons hängen von der Hardware des Computers ab.</span><span class="sxs-lookup"><span data-stu-id="26524-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="26524-114">Verwenden Sie die **Beep** -Methode des **DoCmd** -Objekts, um die **Signalton** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="26524-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

