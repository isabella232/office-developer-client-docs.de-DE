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
ms.localizationpriority: medium
ms.openlocfilehash: 23b34df71d7bef984f16b32dd047aefb3f69d60a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588984"
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

## <a name="finding-the-custom-properties-dialog-box"></a>Suchen des Benutzerdefinierten Eigenschaftendialogfelds

Nicht alle ActiveX-Steuerelemente stellen ein zusätzliches Eigenschaftenfenster bereit. Um herauszufinden, ob ein Steuerelement ein zusätzliches Eigenschaftenfenster bereitstellt, suchen Sie im Microsoft Access-Eigenschaftenfenster für dieses Steuerelement nach der **Custom** -Eigenschaft. Wenn die Liste der Eigenschaften den Namen **Benutzerdefiniert** enthält, stellt das Steuerelement das Dialogfeld Benutzerdefinierte Eigenschaften bereit.

## <a name="using-the-custom-properties-dialog-box"></a>Verwenden des Dialogfelds "Benutzerdefinierte Eigenschaften"

Nachdem Sie das **Benutzerdefinierte** Eigenschaftenfeld im Microsoft Access-Eigenschaftenfenster ausgewählt haben, wählen Sie rechts neben dem Eigenschaftenfeld die Schaltfläche **"Erstellen"** aus, um das benutzerdefinierte Eigenschaftendialogfeld des Steuerelements anzuzeigen, das häufig als Dialogfeld mit Registerkarten angezeigt wird. Choose the tab that contains the interface for setting the properties that you want to set.

Nachdem Sie Änderungen auf einer Registerkarte vorgenommen haben, können Sie diese Änderungen häufig sofort anwenden, indem Sie die Schaltfläche **"Übernehmen"** auswählen (sofern angegeben). Sie können andere Registerkarten auswählen, um andere Eigenschaften nach Bedarf festzulegen. Um alle Änderungen zu genehmigen, die im Dialogfeld "Benutzerdefinierte Eigenschaften" vorgenommen wurden, wählen Sie die Schaltfläche **"OK"** aus. Um zum Microsoft Access-Eigenschaftenblatt zurückzukehren, ohne die Eigenschafteneinstellungen zu ändern, wählen Sie die Schaltfläche **"Abbrechen"** aus.

Sie können das Dialogfeld "Benutzerdefinierte Eigenschaften" auch anzeigen, indem Sie im Menü **"Bearbeiten"** den Unterbefehl **"Eigenschaften"** des Befehls "ActiveX Control **Object"** (z. B. **"Calendar Control Object")** auswählen oder im Kontextmenü für das steuerelement ActiveX dieselbe Unterbefehl auswählen. In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box. Wenn Sie die Schaltfläche **"Erstellen"** auswählen, wird das Dialogfeld "Benutzerdefinierte Eigenschaften" angezeigt, wobei die entsprechende Registerkarte ausgewählt ist (z. B. **Farben).**

