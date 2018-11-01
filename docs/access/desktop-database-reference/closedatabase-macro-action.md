---
title: SchließenDatenbank-Makroaktion
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42ba5925c35081f612bd4a81b49f3c2b16cf61dd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876638"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="a969c-102">SchließenDatenbank-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="a969c-102">CloseDatabase Macro Action</span></span>


<span data-ttu-id="a969c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a969c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a969c-104">Sie können die **SchließenDatenbank** -Aktion zum Schließen der aktuellen Datenbank verwenden.</span><span class="sxs-lookup"><span data-stu-id="a969c-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="a969c-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="a969c-105">Setting</span></span>

<span data-ttu-id="a969c-106">Die **SchließenDatenbank** -Aktion weist keine Argumente auf.</span><span class="sxs-lookup"><span data-stu-id="a969c-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="a969c-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a969c-107">Remarks</span></span>

  - <span data-ttu-id="a969c-108">In Access werden keine Aktionen ausgeführt, die in einem Makro auf die **SchließenDatenbank** -Aktion folgen.</span><span class="sxs-lookup"><span data-stu-id="a969c-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="a969c-109">Diese Aktion hat dieselbe Wirkung wie das Klicken auf die Registerkarte **Datei** , und klicken Sie dann auf **Datenbank schließen**.</span><span class="sxs-lookup"><span data-stu-id="a969c-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="a969c-110">Falls beim Ausführen der **SchließenDatenbank** -Aktion nicht gespeicherte Objekte geöffnet sein sollten, entsprechen die angezeigten Dialogfelder denjenigen, die beim Klicken auf **Datenbank schließen** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a969c-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="a969c-111">Verwenden Sie die **CloseDatabase** -Methode des **DoCmd** -Objekts, um die **SchließenDatenbank** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a969c-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

