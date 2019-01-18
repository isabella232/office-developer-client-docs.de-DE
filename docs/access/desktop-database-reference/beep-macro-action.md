---
title: Signalton-Makroaktion (Access PC-Datenbank-Referenz)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721472"
---
# <a name="beep-macro-action"></a><span data-ttu-id="47788-102">Beep-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="47788-102">Beep macro action</span></span>


<span data-ttu-id="47788-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47788-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47788-104">Sie können die **Signalton** -Aktion verwenden, um einen Signalton über den Lautsprecher des Computers auszugeben.</span><span class="sxs-lookup"><span data-stu-id="47788-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="47788-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="47788-105">Setting</span></span>

<span data-ttu-id="47788-106">Die **Signalton** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="47788-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="47788-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47788-107">Remarks</span></span>

<span data-ttu-id="47788-108">Sie können die **Signalton** -Aktion verwenden, um auf folgende Begebenheiten hinzuweisen:</span><span class="sxs-lookup"><span data-stu-id="47788-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="47788-109">Wichtige Bildschirmänderungen sind aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="47788-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="47788-p101">Es wurden die falsche Arten von Daten in ein Steuerelement eingegeben. Beispielsweise hat der Benutzer numerische Daten in ein Textfeld-Steuerelement eingegeben.</span><span class="sxs-lookup"><span data-stu-id="47788-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="47788-112">Ein Makro hat einen angegebenen Punkt erreicht oder seine Aktionen abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="47788-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="47788-113">Häufigkeit und Dauer des Signaltons hängen von der Hardware des Computers ab.</span><span class="sxs-lookup"><span data-stu-id="47788-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="47788-114">Verwenden Sie die **Beep** -Methode des **DoCmd** -Objekts, um die **Signalton** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="47788-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

