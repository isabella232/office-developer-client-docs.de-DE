---
title: MakroEinzelschritt-Makroaktion
TOCTitle: SingleStep Macro Action
ms:assetid: 2836fe1d-fb9b-6b42-acfd-c52e468161d4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191989(v=office.15)
ms:contentKeyID: 48543855
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm47687
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 747df6327dd73c51722b985c441feca08e1f4f42
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473921"
---
# <a name="singlestep-macro-action"></a>MakroEinzelschritt-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Mit der **MakroEinzelschritt** -Aktion können Sie die Makroausführung anhalten und das Dialogfeld **Einzelschritt** öffnen.

## <a name="setting"></a>Einstellung

Die **MakroEinzelschritt** -Aktion hat keine Argumente.

## <a name="remarks"></a>Hinweise

  - Verwenden Sie die **MakroEinzelschritt** -Aktion, um Probleme mit einem Makro zu beheben, das nicht richtig funktioniert. Sie können die **MakroEinzelschritt** -Aktion direkt vor der Aktion, die Ursache eines Problems sein könnte, einem Makro hinzufügen. Die Aktion hält das Makro an und öffnet das Dialogfeld **Einzelschritt**. In diesem Dialogfeld werden Informationen über das aktuelle Makro angezeigt, z. B. Name des Makros, angegebene Bedingungen, Name der Aktion, Argumente und ggf. die Fehlernummer. Klicken Sie in diesem Dialogfeld auf **Schritt**, um mit der nächsten Makroaktion fortzufahren, auf **Alle Makros anhalten**, um das aktuelle Makro und alle weiteren derzeit ausgeführten Makros anzuhalten, oder auf **Weiter**, um den Einzelschrittmodus zu verlassen und mit der Ausführung des Makros fortzufahren.

  - Die **MakroEinzelschritt** -Aktion hat denselben Effekt wie das Klicken auf **Einzelschritt** auf der Registerkarte **Entwurf** in der Gruppe **Entwurf** des Makro-Generators. Der Unterschied zur **MakroEinzelschritt** -Aktion besteht darin, dass Sie das Makro in der Aktion genau dort positionieren können, wo der Einzelschrittmodus beginnen soll. So müssen Sie nicht alle vorherigen Aktionen ausführen, um zu derjenigen zu gelangen, die Sie genauer untersuchen möchten. Dies ist unerlässlich, wenn Sie vor dem Ausführen des Makros im Makro-Generator auf **Einzelschritt** klicken. In diesem Fall beginnt die Einzelschrittausführung bei der ersten Aktion im Makro.


> [!NOTE]
> <P>[!HINWEIS] Wenn Sie ein Makro mit einzelnen Schritten bis zum Ende ausführen, ohne auf <STRONG>Weiter</STRONG> zu klicken, ist der Einzelschrittmodus auch nach Beenden des Makros noch aktiv. Makros, die Sie anschließend ausführen, werden im Einzelschrittmodus gestartet. Den Einzelschrittmodus können Sie deaktivieren, indem Sie im Dialogfeld <STRONG>Einzelschritt</STRONG> auf <STRONG>Weiter</STRONG> klicken. Sie können auch, während ein Makro in der Entwurfsansicht geöffnet ist, in der Gruppe <STRONG>Tools</STRONG> auf der Registerkarte <STRONG>Entwurf</STRONG> auf <STRONG>Einzelschritt</STRONG> klicken, um diesen Modus zu deaktivieren.</P>


