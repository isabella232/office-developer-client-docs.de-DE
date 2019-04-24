---
title: Dialogfeld für benutzerdefinierte Eigenschaften des ActiveX-Steuerelements
TOCTitle: ActiveX control custom properties dialog box
description: Das zusätzliche Eigenschaftenfenster ist eine Alternative zur Eigenschaftenliste im Microsoft Access-Eigenschaftenfenster zum Einstellen der Eigenschaften des ActiveX-Steuerelements in der Entwurfsansicht.
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4574abc86e6eacd38721e601d26c8b8fbf0a0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314105"
---
# <a name="activex-control-custom-properties-dialog-box"></a>Dialogfeld für benutzerdefinierte Eigenschaften des ActiveX-Steuerelements

**Gilt für**: Access 2013, Office 2013

Wenn Sie die Eigenschaften eines ActiveX-Steuerelements einstellen, möchten Sie möglicherweise das zusätzliche Eigenschaftenfenster des Steuerelements verwenden. Das zusätzliche Eigenschaftenfenster ist eine Alternative zur Eigenschaftenliste im Microsoft Access-Eigenschaftenfenster zum Einstellen der Eigenschaften des ActiveX-Steuerelements in der Entwurfsansicht.

> [!NOTE]
> [!HINWEIS] Diese Informationen betreffen nur ActiveX-Steuerelemente in einer Microsoft Access-Datenbankumgebung.

## <a name="two-ways-to-set-properties"></a>Zwei Möglichkeiten zum Festlegen von Eigenschaften

Der Grund für das Vorhandensein des zusätzlichen Eigenschaftenfensters besteht darin, dass nicht alle Anwendungen, die ActiveX-Steuerelemente benutzen, ein Eigenschaftenfenster wie das von Microsoft Access besitzen. Das zusätzliche Eigenschaftenfenster stellt eine Schnittstelle zum Einstellen der wichtigsten Steuerelementeigenschaften bereit, unabhängig von der Oberfläche der Host-Anwendung.

Die Eigenschaften einiger ActiveX-Steuerelemente können Sie in beiden Eigenschaftenfenstern festlegen:

- Im Microsoft Access-Eigenschaftenfenster
- Im zusätzlichen Eigenschaftenfenster eines ActiveX-Steuerelements

In einigen Fällen können Sie nur das zusätzliche Eigenschaftenfenster zum Einstellen einer Eigenschaft in der Entwurfsansicht verwenden. Dies ist normalerweise dann der Fall, wenn die Schnittstelle, die zum Einstellen einer Eigenschaft benötigt wird, nicht innerhalb des Microsoft Access-Eigenschaftenfensters funktioniert. Beispielsweise besitzt die Eigenschaft **GridFont** des Kalender-Steuerelements mehrere Argumente; Sie können jedoch im Microsoft Access-Eigenschaftenfenster nur ein Argument pro Eigenschaft einstellen.

## <a name="finding-the-custom-properties-dialog-box"></a>Suchen des Dialogfelds "benutzerdefinierte Eigenschaften"

Nicht alle ActiveX-Steuerelemente stellen ein zusätzliches Eigenschaftenfenster bereit. Um herauszufinden, ob ein Steuerelement ein zusätzliches Eigenschaftenfenster bereitstellt, suchen Sie im Microsoft Access-Eigenschaftenfenster für dieses Steuerelement nach der **Custom** -Eigenschaft. Wenn die Liste der Eigenschaften den Namen **Custom**enthält, stellt das Steuerelement das Dialogfeld Benutzerdefinierte Eigenschaften bereit.

## <a name="using-the-custom-properties-dialog-box"></a>Verwenden des Dialogfelds "benutzerdefinierte Eigenschaften"

Nachdem Sie das Feld **benutzerdefinierte** Eigenschaft im Microsoft Access-Eigenschaftenfenster ausgewählt haben, wählen Sie die **Generator** -Schaltfläche rechts neben dem Eigenschaftenfeld aus, um das Dialogfeld Benutzerdefinierte Eigenschaften des Steuerelements anzuzeigen, das häufig als Registerkarten Dialogfeld angezeigt wird. Choose the tab that contains the interface for setting the properties that you want to set.

Nachdem Sie auf einer Registerkarte Änderungen vorgenommen haben, können Sie diese Änderungen häufig sofort anwenden, indem Sie die Schaltfläche über **nehmen** (sofern angegeben) auswählen. Sie können andere Registerkarten auswählen, um bei Bedarf andere Eigenschaften festzulegen. Um alle Änderungen im Dialogfeld Benutzerdefinierte Eigenschaften zu genehmigen, klicken Sie auf die Schaltfläche **OK** . Um zur Microsoft Access-Eigenschaftenseite zurückzukehren, ohne Eigenschaftseinstellungen zu ändern, klicken Sie auf die Schaltfläche **Abbrechen** .

Sie können das Dialogfeld Benutzerdefinierte Eigenschaften auch anzeigen, indem Sie den unter Befehl **Eigenschaften** des ActiveX-Steuerelement **Objekt** -Befehls (beispielsweise **Calendar-Steuerelementobjekt**) im Menü **Bearbeiten** auswählen oder denselben unter Befehl auf das Kontextmenü für das ActiveX-Steuerelement. In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box. Wenn Sie die **Generator** -Schaltfläche auswählen, wird das Dialogfeld Benutzerdefinierte Eigenschaften mit der entsprechenden Registerkarte (beispielsweise **Farben**) angezeigt.

