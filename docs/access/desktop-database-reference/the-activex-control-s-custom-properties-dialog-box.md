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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712135"
---
# <a name="activex-control-custom-properties-dialog-box"></a>Dialogfeld für benutzerdefinierte Eigenschaften des ActiveX-Steuerelements

**Betrifft**: Access 2013, Office 2013

Wenn Sie die Eigenschaften eines ActiveX-Steuerelements einstellen, möchten Sie möglicherweise das zusätzliche Eigenschaftenfenster des Steuerelements verwenden. Das zusätzliche Eigenschaftenfenster ist eine Alternative zur Eigenschaftenliste im Microsoft Access-Eigenschaftenfenster zum Einstellen der Eigenschaften des ActiveX-Steuerelements in der Entwurfsansicht.

> [!NOTE]
> [!HINWEIS] Diese Informationen betreffen nur ActiveX-Steuerelemente in einer Microsoft Access-Datenbankumgebung.

## <a name="two-ways-to-set-properties"></a>Zwei Methoden zum Festlegen von Eigenschaften

Der Grund für das Vorhandensein des zusätzlichen Eigenschaftenfensters besteht darin, dass nicht alle Anwendungen, die ActiveX-Steuerelemente benutzen, ein Eigenschaftenfenster wie das von Microsoft Access besitzen. Das zusätzliche Eigenschaftenfenster stellt eine Schnittstelle zum Einstellen der wichtigsten Steuerelementeigenschaften bereit, unabhängig von der Oberfläche der Host-Anwendung.

Die Eigenschaften einiger ActiveX-Steuerelemente können Sie in beiden Eigenschaftenfenstern festlegen:

- Im Microsoft Access-Eigenschaftenfenster
- Im zusätzlichen Eigenschaftenfenster eines ActiveX-Steuerelements

In einigen Fällen können Sie nur das zusätzliche Eigenschaftenfenster zum Einstellen einer Eigenschaft in der Entwurfsansicht verwenden. Dies ist normalerweise dann der Fall, wenn die Schnittstelle, die zum Einstellen einer Eigenschaft benötigt wird, nicht innerhalb des Microsoft Access-Eigenschaftenfensters funktioniert. Beispielsweise besitzt die Eigenschaft **GridFont** des Kalender-Steuerelements mehrere Argumente; Sie können jedoch im Microsoft Access-Eigenschaftenfenster nur ein Argument pro Eigenschaft einstellen.

## <a name="finding-the-custom-properties-dialog-box"></a>Suchen des zusätzlichen Eigenschaftenfensters

Nicht alle ActiveX-Steuerelemente stellen ein zusätzliches Eigenschaftenfenster bereit. Um herauszufinden, ob ein Steuerelement ein zusätzliches Eigenschaftenfenster bereitstellt, suchen Sie im Microsoft Access-Eigenschaftenfenster für dieses Steuerelement nach der **Custom** -Eigenschaft. Wenn die Liste der Eigenschaften der Name **Benutzerdefiniert**enthält, enthält das Steuerelement das Dialogfeld Benutzerdefinierte Eigenschaften.

## <a name="using-the-custom-properties-dialog-box"></a>Verwenden das Dialogfeld Benutzerdefinierte Eigenschaften

Nachdem Sie das **benutzerdefinierte** Eigenschaftenfeld im Eigenschaftenfenster Microsoft Access auswählen, wählen Sie die **Generator** -Schaltfläche rechts neben dem Eigenschaftenfeld des Steuerelements Eigenschaftenfensters, häufig, die als ein Dialogfeld angezeigt. Wählen Sie die Registerkarte mit der Oberfläche zum Festlegen der Eigenschaften, die Sie festlegen möchten.

Nachdem Sie auf einer Registerkarte Änderungen vorgenommen haben, können Sie häufig diese Änderungen sofort anwenden indem Sie auf die Schaltfläche **Übernehmen** (falls bereitgestellt). Sie können andere Registerkarten, um andere Eigenschaften festzulegen, wie gewünscht auswählen. Wählen Sie die Schaltfläche **OK** , um alle Änderungen im Dialogfeld Benutzerdefinierte Eigenschaften zu genehmigen. Um auf die Microsoft Access-Eigenschaftenfenster zurückzukehren, ohne alle Einstellungen ändern, wählen Sie die Schaltfläche **Abbrechen** .

Sie können auch die zusätzlichen Eigenschaftenfensters durch Auswählen von Unterbefehl **Eigenschaften** des ActiveX-Steuerelements **-(beispielsweise **Calendar Control-Objekt**)** im Menü **Bearbeiten** oder indem Sie auf diesen Unterbefehl auf anzeigen das Kontextmenü für das ActiveX-Steuerelement. Darüber hinaus müssen einige Eigenschaften in der Microsoft Access-Eigenschaftenfenster für das ActiveX-Steuerelement, wie die **GridFontColor** -Eigenschaft das Kalender-Steuerelement eine **Generator** -Schaltfläche rechts neben dem Eigenschaftenfeld. Wenn Sie auf die **Generator** -Schaltfläche auswählen, wird das Dialogfeld Benutzerdefinierte Eigenschaften mit der entsprechenden Registerkarte ausgewählt (beispielsweise **Farben**) angezeigt.

