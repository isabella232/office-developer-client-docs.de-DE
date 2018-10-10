---
title: Zusätzlichen Eigenschaftenfensters eines ActiveX-Steuerelements
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474652"
---
# <a name="activex-controls-custom-properties-dialog-box"></a>Zusätzlichen Eigenschaftenfensters eines ActiveX-Steuerelements

**Betrifft**: Access 2013 | Office 2013

Wenn Sie die Eigenschaften eines ActiveX-Steuerelements einstellen, möchten Sie möglicherweise das zusätzliche Eigenschaftenfenster des Steuerelements verwenden. Das zusätzliche Eigenschaftenfenster ist eine Alternative zur Eigenschaftenliste im Microsoft Access-Eigenschaftenfenster zum Einstellen der Eigenschaften des ActiveX-Steuerelements in der Entwurfsansicht.

> [!NOTE]
> [!HINWEIS] Diese Informationen betreffen nur ActiveX-Steuerelemente in einer Microsoft Access-Datenbankumgebung.



## <a name="two-ways-to-set-properties"></a>Zwei Möglichkeiten zum Einstellen von Eigenschaften

Der Grund für das Vorhandensein des zusätzlichen Eigenschaftenfensters besteht darin, dass nicht alle Anwendungen, die ActiveX-Steuerelemente benutzen, ein Eigenschaftenfenster wie das von Microsoft Access besitzen. Das zusätzliche Eigenschaftenfenster stellt eine Schnittstelle zum Einstellen der wichtigsten Steuerelementeigenschaften bereit, unabhängig von der Oberfläche der Host-Anwendung.

Die Eigenschaften einiger ActiveX-Steuerelemente können Sie in beiden Eigenschaftenfenstern festlegen:

  - Im Microsoft Access-Eigenschaftenfenster

  - Im zusätzlichen Eigenschaftenfenster eines ActiveX-Steuerelements

In einigen Fällen können Sie nur das zusätzliche Eigenschaftenfenster zum Einstellen einer Eigenschaft in der Entwurfsansicht verwenden. Dies ist normalerweise dann der Fall, wenn die Schnittstelle, die zum Einstellen einer Eigenschaft benötigt wird, nicht innerhalb des Microsoft Access-Eigenschaftenfensters funktioniert. Beispielsweise besitzt die Eigenschaft **GridFont** des Kalender-Steuerelements mehrere Argumente; Sie können jedoch im Microsoft Access-Eigenschaftenfenster nur ein Argument pro Eigenschaft einstellen.

## <a name="finding-the-custom-properties-dialog-box"></a>Suchen des zusätzlichen Eigenschaftenfensters

Nicht alle ActiveX-Steuerelemente stellen ein zusätzliches Eigenschaftenfenster bereit. Um herauszufinden, ob ein Steuerelement ein zusätzliches Eigenschaftenfenster bereitstellt, suchen Sie im Microsoft Access-Eigenschaftenfenster für dieses Steuerelement nach der **Custom** -Eigenschaft. Wenn in der Liste der Eigenschaften der Name **Benutzerdefiniert** enthalten ist, stellt das Steuerelement das zusätzliche Eigenschaftenfenster bereit.

## <a name="using-the-custom-properties-dialog-box"></a>Verwenden des zusätzlichen Eigenschaftenfensters

Klicken Sie im Microsoft Access-Eigenschaftenfenster auf das Eigenschaftenfeld **Benutzerdefiniert** und anschließend auf die** **Generator-Schaltfläche rechts neben dem Eigenschaftenfeld, um das zusätzliche Eigenschaftenfenster des Steuerelements anzuzeigen. Es wird häufig als Dialogfeld mit Registerkarten dargestellt. Klicken Sie auf die entsprechende Registerkarte zum Festlegen der gewünschten Eigenschaften.

Nachdem Sie Änderungen auf einer Registerkarte vorgenommen haben, können Sie diese Änderungen häufig direkt anwenden, indem Sie auf die Schaltfläche **Übernehmen** (falls vorhanden) klicken. Sie können auch auf andere Registerkarten klicken, um bei Bedarf weitere Eigenschaften festzulegen. Damit alle im zusätzlichen Eigenschaftenfenster vorgenommenen Änderungen wirksam werden, klicken Sie auf die Schaltfläche **OK**. Wenn Sie zum Microsoft Access-Eigenschaftenfenster zurückkehren möchten, ohne Eigenschafteneinstellungen zu ändern, klicken Sie auf die Schaltfläche **Abbrechen**.

Sie können das zusätzliche Eigenschaftenfenster auch anzeigen, indem Sie im Menü **Bearbeiten** auf den Eintrag für das ActiveX-Steuerelement (z. B. **Kalender**-**Objekt**) und dann auf den Unterbefehl **Eigenschaften** klicken, oder indem Sie im Kontextmenü des ActiveX-Steuerelements auf diesen Unterbefehl klicken. Außerdem besitzen einige Eigenschaften, wie z. B. die **GridFontColor**-Eigenschaft, im Microsoft Access-Eigenschaftenfenster für das ActiveX-Steuerelement eine** **Generator-Schaltfläche rechts neben dem Eigenschaftenfeld. Wenn Sie auf die** **Generator-Schaltfläche klicken, wird das zusätzliche Eigenschaftenfenster angezeigt, wobei die entsprechende Registerkarte (z. B. **Farbe**) ausgewählt ist.

