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
ms.localizationpriority: medium
ms.openlocfilehash: f9ff8558160d8815651c4b386297469227c81b73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589120"
---
# <a name="singlestep-macro-action"></a>SingleStep-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **MakroEinzelschritt**-Aktion können Sie die Makroausführung anhalten und das Dialogfeld **Einzelschritt** öffnen.

## <a name="setting"></a>Einstellung

Die **MakroEinzelschritt**-Aktion hat keine Argumente.

## <a name="remarks"></a>HinwBemerkungeneise

- Verwenden Sie die **MakroEinzelschritt** -Aktion, um Probleme mit einem Makro zu beheben, das nicht richtig funktioniert. Sie können die **MakroEinzelschritt** -Aktion direkt vor der Aktion, die Ursache eines Problems sein könnte, einem Makro hinzufügen. Die Aktion hält das Makro an und öffnet das Dialogfeld **Einzelschritt**. In diesem Dialogfeld werden Informationen über das aktuelle Makro angezeigt, z. B. Name des Makros, angegebene Bedingungen, Name der Aktion, Argumente und ggf. die Fehlernummer. Klicken Sie in diesem Dialogfeld auf **Schritt**, um mit der nächsten Makroaktion fortzufahren, auf **Alle Makros anhalten**, um das aktuelle Makro und alle weiteren derzeit ausgeführten Makros anzuhalten, oder auf **Weiter**, um den Einzelschrittmodus zu verlassen und mit der Ausführung des Makros fortzufahren.

- Die **MakroEinzelschritt** -Aktion hat denselben Effekt wie das Klicken auf **Einzelschritt** auf der Registerkarte **Entwurf** in der Gruppe **Entwurf** des Makro-Generators. Der Unterschied zur **MakroEinzelschritt** -Aktion besteht darin, dass Sie das Makro in der Aktion genau dort positionieren können, wo der Einzelschrittmodus beginnen soll. So müssen Sie nicht alle vorherigen Aktionen ausführen, um zu derjenigen zu gelangen, die Sie genauer untersuchen möchten. Dies ist unerlässlich, wenn Sie vor dem Ausführen des Makros im Makro-Generator auf **Einzelschritt** klicken. In diesem Fall beginnt die Einzelschrittausführung bei der ersten Aktion im Makro.

> [!NOTE]
> [!HINWEIS] Wenn Sie ein Makro mit einzelnen Schritten bis zum Ende ausführen, ohne auf **Weiter** zu klicken, ist der Einzelschrittmodus auch nach Beenden des Makros noch aktiv. Makros, die Sie anschließend ausführen, werden im Einzelschrittmodus gestartet. Den Einzelschrittmodus können Sie deaktivieren, indem Sie im Dialogfeld **Einzelschritt** auf **Weiter** klicken. Sie können auch, während ein Makro in der Entwurfsansicht geöffnet ist, in der Gruppe **Tools** auf der Registerkarte **Entwurf** auf **Einzelschritt** klicken, um diesen Modus zu deaktivieren.
