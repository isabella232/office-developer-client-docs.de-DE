---
title: SingleStep-Makroaktion
TOCTitle: SingleStep macro action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b50fe7e37cfe79a54574e54e720cbad2ef84a14e
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998252"
---
# <a name="singlestep-macro-action"></a><span data-ttu-id="5bc85-102">SingleStep-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="5bc85-102">SingleStep macro action</span></span>

<span data-ttu-id="5bc85-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bc85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bc85-104">Mit der **MakroEinzelschritt** -Aktion können Sie die Makroausführung anhalten und das Dialogfeld **Einzelschritt** öffnen.</span><span class="sxs-lookup"><span data-stu-id="5bc85-104">You can use the **SingleStep** action to pause macro execution and open the **Macro Single Step** dialog box.</span></span>

## <a name="setting"></a><span data-ttu-id="5bc85-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="5bc85-105">Setting</span></span>

<span data-ttu-id="5bc85-106">Die **MakroEinzelschritt** -Aktion hat keine Argumente.</span><span class="sxs-lookup"><span data-stu-id="5bc85-106">The **SingleStep** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc85-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5bc85-107">Remarks</span></span>

- <span data-ttu-id="5bc85-p101">Verwenden Sie die **MakroEinzelschritt** -Aktion, um Probleme mit einem Makro zu beheben, das nicht richtig funktioniert. Sie können die **MakroEinzelschritt** -Aktion direkt vor der Aktion, die Ursache eines Problems sein könnte, einem Makro hinzufügen. Die Aktion hält das Makro an und öffnet das Dialogfeld **Einzelschritt**. In diesem Dialogfeld werden Informationen über das aktuelle Makro angezeigt, z. B. Name des Makros, angegebene Bedingungen, Name der Aktion, Argumente und ggf. die Fehlernummer. Klicken Sie in diesem Dialogfeld auf **Schritt**, um mit der nächsten Makroaktion fortzufahren, auf **Alle Makros anhalten**, um das aktuelle Makro und alle weiteren derzeit ausgeführten Makros anzuhalten, oder auf **Weiter**, um den Einzelschrittmodus zu verlassen und mit der Ausführung des Makros fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="5bc85-p101">Use the **SingleStep** action to troubleshoot a macro that is not working properly. You can add the **SingleStep** action to a macro just before an action that you suspect may be the cause of the problem. The action pauses the macro and opens the **Macro Single Step** dialog box. This dialog box displays information about the current macro action, such as the macro name, any specified conditions, the action name, arguments, and the error number, if applicable. In the dialog box, you can click **Step** to advance to the next macro action, **Stop All Macros** to stop the current macro and any other macros that are running, or **Continue** to stop single stepping and resume normal operation of the macro.</span></span>

- <span data-ttu-id="5bc85-p102">Die **MakroEinzelschritt** -Aktion hat denselben Effekt wie das Klicken auf **Einzelschritt** auf der Registerkarte **Entwurf** in der Gruppe **Entwurf** des Makro-Generators. Der Unterschied zur **MakroEinzelschritt** -Aktion besteht darin, dass Sie das Makro in der Aktion genau dort positionieren können, wo der Einzelschrittmodus beginnen soll. So müssen Sie nicht alle vorherigen Aktionen ausführen, um zu derjenigen zu gelangen, die Sie genauer untersuchen möchten. Dies ist unerlässlich, wenn Sie vor dem Ausführen des Makros im Makro-Generator auf **Einzelschritt** klicken. In diesem Fall beginnt die Einzelschrittausführung bei der ersten Aktion im Makro.</span><span class="sxs-lookup"><span data-stu-id="5bc85-p102">The **SingleStep** action has a similar effect to clicking **Single Step** in the **Tools** group on the **Design** tab of the Macro Builder. The difference between doing this and running the **SingleStep** action is that by running the action, you can place the action in the macro exactly where you want single stepping to begin. That way, you don't have to step through all the previous actions to get to the one you want to examine. On the other hand, when you click **Single Step** in the Macro Builder, you must do so before running the macro. In that case, single stepping begins at the first action in the macro.</span></span>

> [!NOTE]
> <span data-ttu-id="5bc85-p103">[!HINWEIS] Wenn Sie ein Makro mit einzelnen Schritten bis zum Ende ausführen, ohne auf **Weiter** zu klicken, ist der Einzelschrittmodus auch nach Beenden des Makros noch aktiv. Makros, die Sie anschließend ausführen, werden im Einzelschrittmodus gestartet. Den Einzelschrittmodus können Sie deaktivieren, indem Sie im Dialogfeld **Einzelschritt** auf **Weiter** klicken. Sie können auch, während ein Makro in der Entwurfsansicht geöffnet ist, in der Gruppe **Tools** auf der Registerkarte **Entwurf** auf **Einzelschritt** klicken, um diesen Modus zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5bc85-p103">If you single-step all the way to the end of a macro without clicking **Continue**, single stepping will still be in effect when the macro ends. Any subsequent macro you run will start in single step mode. To turn off single stepping, either click **Continue** in the **Macro Single Step** dialog box, or, with a macro open in Design view, on the **Design** tab, in the **Tools** group, click **Single Step** so that it is no longer selected.</span></span>