---
title: Problembehandlung von Formularvorlagen, die das InfoPath-Objektmodell zur Entwurfszeit verwenden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Entwurfszeit InfoPath 2003-kompatible Formularvorlagen, Problembehandlung zur Entwurfszeit, Problembehandlung von Formularvorlagen [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4179b235-e21d-4c37-ae2b-ad01388296ec
description: Die folgenden Abschnitte beschreiben allgemeine Problembehandlungsszenarien, die Sie beim Entwerfen und Debuggen von Formularvorlagen, die durch die Microsoft.Office.Interop.InfoPath.SemiTrust bereitgestellte InfoPath 2003-kompatible Objektmodell verwenden verwaltetem Code auftreten können Namespace.
ms.openlocfilehash: af71c8058744561a4c8ee0870fb37054e9979751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790839"
---
# <a name="troubleshoot-form-templates-that-use-the-infopath-object-model-at-design-time"></a>Problembehandlung von Formularvorlagen, die das InfoPath-Objektmodell zur Entwurfszeit verwenden

Die folgenden Abschnitte beschreiben allgemeine Problembehandlungsszenarien, die Sie beim Entwerfen und Debuggen von Formularvorlagen, die durch die **bereitgestellte InfoPath 2003-kompatible Objektmodell verwenden verwaltetem Code auftreten können Microsoft.Office.Interop.InfoPath.SemiTrust** Namespace. 
  
## <a name="cannot-preview-or-debug-form-templates-that-use-calls-to-object-model-security-level-3-methods-and-properties"></a>Das Anzeigen der Vorschau oder Debuggen von Formularvorlagen, die Aufrufe der Methoden und Eigenschaften der Objektmodell-Sicherheitsebene 3 verwenden, ist nicht möglich

Wenn Sie versuchen, zu debuggen oder Preview vertraut ein Projekt mit verwaltetem Code, die Code enthält, die Elemente des Objektmodells aufruft, die eine vollständige erfordern, InfoPath zeigt die Fehlermeldung "eine nicht behandelte Sicherheitsausnahme ist im Formularcode aufgetreten" und das Formular kann nicht geöffnet werden . Damit können Geschäftslogik in der Formularvorlage, gedebuggt oder eine Vorschau angezeigt werden soll, müssen Sie die Sicherheitsstufe **Voll** vertrauenswürdig festgelegt und die Formularvorlage digital signieren. Weitere Informationen zur Vorgehensweise finden Sie unter [Anzeigen der Vorschau und Debuggen von Formularvorlagen, erfordern voll vertrauenswürdig](how-to-preview-and-debug-form-templates-that-require-full-trust.md).
  
## <a name="cannot-update-xpath-expressions-in-event-handlers-if-the-matchpath-parameter-value-was-deleted-manually"></a>XPath-Ausdrücke in Ereignishandlern können nicht aktualisiert werden, wenn der Wert des MatchPath-Parameters manuell gelöscht wurde

Wenn Sie einen Ereignishandler an ein Feld oder Gruppe hinzufügen und das Schema der Datenquelle im Aufgabenbereich InfoPath- **Felder** in eine Möglichkeit, die dieses Feld oder Gruppe wirkt sich auf (beispielsweise durch Umbenennen oder verschieben) später ändern, wird eine Meldung angezeigt werden gefragt, ob Sie Updat möchten der XPath-Ausdruck e Ausdrücke in Code des Formulars. Die XPath-Ausdrücke, die in dieser Nachricht bezeichnet wird sind in der [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) -Parameters des Attributs [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) angegebenen Werte verwendet werden, die ein Feld oder eine Gruppe in der Datenquelle des Formulars den Ereignishandler zugeordnet . Keine anderen XPath-Ausdrücke in Ihrem Code werden aktualisiert. Der Algorithmus zum Aktualisieren der XPath-Ausdrücke hängt einen Wert, dass Sie sich im **MatchPath** -Parameter der **InfoPathEventHandler** Attribute, die im Formularcode angewendet werden. Wenn Sie diese Werte manuell gelöscht, bevor Sie Antworten auf die Aufforderung zum Aktualisieren von XPath-Ausdrücken, werden InfoPath nicht können die XPath-Ausdrücke automatisch aktualisiert. Weitere Informationen finden Sie unter [Hinzufügen einer Event Handler mithilfe des InfoPath 2003-Objektmodells](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="cannot-call-members-of-the-infopath-2003-compatible-object-model-on-a-separate-thread"></a>Member des InfoPath 2003-kompatiblen Objektmodells können nicht in einem getrennten Thread aufgerufen werden

Das InfoPath 2003-kompatible Objektmodell unterstützt keine Aufrufe in einem getrennten Thread. Beispielsweise wird der folgende Code, der Ruft eine Funktion mit dem Namen LaunchOMFunction, die Mitglieder des InfoPath-Objektmodells aufruft, nicht ausgeführt. 
  
```cs
Thread th = new Thread(new ThreadStart(LaunchOMFunction));
th.Start();
```

Bei Bedarf ist es eine Möglichkeit, diese Einschränkung umgehen. Informationen finden Sie unter [Threading-Unterstützung in InfoPath Projekte mithilfe des InfoPath 2003-Objektmodells](threading-support-in-infopath-projects-using-the-infopath-2003-object-model.md).
  
## <a name="omitting-optional-parameters-causes-a-build-error-in-visual-basic-and-visual-c"></a>Das Auslassen optionaler Parameter verursacht einen Buildfehler in Visual Basic und Visual C#

Wenn ein InfoPath-Objektmodellmember einen optionalen Parameter enthält, und Sie einen Wert für diesen Parameter nicht angeben, müssen Sie stattdessen das Feld **Type.Missing** für diesen Parameter übergeben. Installationsfehler, Feld **Type.Missing** übergeben, wenn Sie ein Istwert ausgelassen wird, in einen Buildfehler bewirken. Dies gilt für geschrieben in Visual Basic und Visual C#-Code. Weitere Informationen und Beispiele finden Sie im Abschnitt "Übergeben Optionaler Parameter an InfoPath-Objektmodellmember" im Thema [InfoPath 2003 kompatible Objektmodelle](infopath-2003-compatible-object-models.md) . 
  
## <a name="see-also"></a>Siehe auch

- [Informationen zum Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md)
- [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md)
- [Behandeln von Fehlern mit dem InfoPath 2003-Objektmodell](how-to-handle-errors-using-the-infopath-2003-object-model.md)
- [Anzeigen der Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md)
- [Debuggen von InfoPath-Projekten mit dem InfoPath 2003-Objektmodell](how-to-debug-infopath-projects-using-the-infopath-2003-object-model.md)

