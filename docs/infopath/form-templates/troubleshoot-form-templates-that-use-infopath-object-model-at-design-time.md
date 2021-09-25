---
title: Problembehandlung bei Formularvorlagen, die das InfoPath-Objektmodell zur Entwurfszeit verwenden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, Problembehandlung zur Entwurfszeit, Problembehandlung bei Formularvorlagen [InfoPath 2007], Entwurfszeit
ms.localizationpriority: medium
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: Die folgenden Abschnitte beschreiben allgemeine Problembehandlungsszenarien, die beim Entwerfen und Debuggen von Formularvorlagen mit verwaltetem Code auftreten können, die das vom Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace bereitgestellte InfoPath 2003-kompatible Objektmodell verwenden.
ms.openlocfilehash: 37e92034f9d543c2cc12f404d85726d9435877fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614507"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Problembehandlung bei Formularvorlagen, die das InfoPath-Objektmodell zur Entwurfszeit verwenden

Die folgenden Abschnitte beschreiben allgemeine Problembehandlungsszenarien, die beim Entwerfen und Debuggen von Formularvorlagen mit verwaltetem Code auftreten können, die das vom **Microsoft.Office.Interop.InfoPath.SemiTrust**-Namespace bereitgestellte InfoPath 2003-kompatible Objektmodell verwenden. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Das Anzeigen der Vorschau oder Debuggen von Formularvorlagen, die Aufrufe der Methoden und Eigenschaften der Objektmodell-Sicherheitsebene 3 verwenden, ist nicht möglich

Beim Versuch, ein Projekt mit verwaltetem Code zu debuggen oder in der Vorschau anzuzeigen, das Code zum Aufrufen von Objektmodellmembern enthält, die volle Vertrauenswürdigkeit erfordern, zeigt InfoPath eine Fehlermeldung an, die besagt, dass eine unbehandelte Sicherheitsausnahme im Formularcode aufgetreten ist, und das Formular wird nicht geöffnet. Um das Debuggen oder die Vorschau von Geschäftslogik in der Formularvorlage zu ermöglichen, müssen Sie die Sicherheitsebene auf **Voll vertrauenswürdig** festlegen und die Formularvorlage digital signieren. Ausführliche Informationen hierzu finden Sie unter Vorschau und Debuggen von [Formularvorlagen, die voll vertrauenswürdig sein müssen.](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>XPath-Ausdrücke in Ereignishandlern können nicht aktualisiert werden, wenn der Wert des MatchPath-Parameters manuell gelöscht wurde

Wenn Sie einem Feld oder einer Gruppe einen Ereignishandler hinzufügen und später  das Schema der Datenquelle im InfoPath Fields-Aufgabenbereich so ändern, dass es sich auf dieses Feld oder diese Gruppe auswirkt (z. B. durch Umbenennen oder Verschieben), wird eine Meldung angezeigt, in der Sie gefragt werden, ob Sie die XPath-Ausdrücke im Formularcode aktualisieren möchten. Die in dieser Nachricht genannten XPath-Ausdrücke sind die im [MatchPath-Parameter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) des [InfoPathEventHandlerAttribute-Attributs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) angegebenen Werte, die verwendet werden, um den Ereignishandler einem Feld oder einer Gruppe in der Datenquelle des Formulars zuzuordnen. Es werden keine anderen XPath-Ausdrücke in Ihrem Code aktualisiert. Der Algorithmus zum Aktualisieren der XPath-Ausdrücke hängt von einem Wert ab, der im **MatchPath-Parameter** der **InfoPathEventHandler-Attribute** vorhanden ist, die im Formularcode angewendet werden. Wenn Sie diese Werte manuell gelöscht haben, bevor Sie auf die Aufforderung zum Aktualisieren von XPath-Ausdrücken reagieren, kann InfoPath die XPath-Ausdrücke nicht automatisch aktualisieren. Weitere Informationen finden Sie unter [Hinzufügen eines Ereignishandlers mithilfe des InfoPath 2003-Objektmodells.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Member des InfoPath 2003-kompatiblen Objektmodells können nicht in einem getrennten Thread aufgerufen werden

Das InfoPath 2003-kompatible Objektmodell unterstützt keine Aufrufe in einem getrennten Thread. Der folgende Code beispielsweise, der die Funktion LaunchOMFunction aufruft, die wiederum Member des InfoPath-Objektmodells aufruft, wird nicht ausgeführt. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

Es gibt eine Möglichkeit zum Umgehen dieser Einschränkung. Weitere Informationen finden Sie unter [Threadunterstützung in InfoPath-Projekten mithilfe des InfoPath 2003-Objektmodells.](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md)
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>Das Auslassen optionaler Parameter verursacht einen Buildfehler in Visual Basic und Visual C#

Wenn ein InfoPath-Objektmodellmember einen optionalen Parameter enthält und Sie keinen Wert für diesen Parameter angeben, müssen Sie für den Parameter stattdessen das Feld **Type.Missing** übergeben. Erfolgt keine Übergabe des Felds **Type.Missing**, führt das Auslassen eines tatsächlichen Werts zu einem Buildfehler. Dies gilt sowohl für in Visual Basic als auch in Visual C# geschriebenen Code. Weitere Informationen und Beispiele finden Sie im Abschnitt "Übergeben optionaler Parameter an InfoPath-Objektmodellmember" im Thema ["InfoPath 2003 Compatible Object Models".](infopath-2003-compatible-object-models.md) 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)
- [Behandeln von Fehlern mithilfe des InfoPath 2003-Objektmodells](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Anzeigen einer Vorschau und Debuggen von Formularvorlagen, die vollständig vertrauenswürdig sein müssen](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Debuggen von InfoPath-Projekten mithilfe des InfoPath 2003-Objektmodells](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

