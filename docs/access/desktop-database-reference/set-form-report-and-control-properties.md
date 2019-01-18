---
title: Einstellen von Formular-, Berichts- und Steuerelementeigenschaften
TOCTitle: Set form, report, and control properties
description: Jedes Formular, Bericht, Abschnitt und Steuerelement verfügt über die Einstellungen, die Sie bearbeiten können, um das Aussehen und das Verhalten des betreffenden Elements auf bestimmten in Access 2013 ändern.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701690"
---
# <a name="set-form-report-and-control-properties"></a>Einstellen von Formular-, Berichts- und Steuerelementeigenschaften

**Betrifft**: Access 2013, Office 2013

Jedes Formular, jeder Bericht, jeder Bereich und jedes Steuerelement verfügt über Eigenschafteneinstellungen, mit denen Sie das Aussehen und die Funktionsweise eines Elements ändern können. Sie können die Eigenschaften im Eigenschaftenfenster, in einem Makro oder in Visual Basic anzeigen und ändern.

## <a name="set-properties"></a>Eigenschaften festlegen

1. Wählen Sie in der Formularentwurfsansicht oder Berichtsentwurfsansicht das Steuerelement, den Bereich, das Formular oder den Bericht aus, für das bzw. den Sie die Eigenschaft einstellen möchten. Sie haben folgende Auswahlmöglichkeiten:
    
   - Steuerelemente. Zum Auswählen mehrerer Steuerelemente die UMSCHALTTASTE gedrückt halten Sie und wählen Sie die Steuerelemente, oder ziehen Sie den Mauszeiger über die Steuerelemente, die Sie auswählen möchten. Wenn Sie mehrere Steuerelemente auswählen, zeigt das Eigenschaftenfenster nur die Eigenschaften an, die alle markierten Steuerelemente gemeinsam besitzen.
    
   - Einen Bereich. Wählen Sie die Bereichsauswahl des Abschnitts, den Sie auswählen möchten.
    
   - Das gesamte Formular oder den Bericht. Wählen Sie die Formular- oder Berichtsauswahl in der oberen linken Ecke des Formulars oder Berichts.

2. Anzuzeigen Sie das Eigenschaftenfenster durch das Objekt oder den Bereich mit der rechten Maustaste, und klicken Sie dann im Kontextmenü auf **Eigenschaften** auswählen oder durch Auswählen von **Eigenschaften** auf der Symbolleiste.

3. Wählen Sie die Eigenschaft für die Sie den Wert festlegen möchten, und führen Sie dann eine der folgenden:
    
   - Geben Sie im Einstellungsfeld der Eigenschaft die gewünschte Einstellung oder einen geeigneten Ausdruck ein.
    
   - Wenn das Einstellungsfeld der Eigenschaft einen Pfeil enthält, wählen Sie den Pfeil, und wählen Sie dann einen Wert in der Liste.
    
   - Wenn eine **Generator** -Schaltfläche rechts neben dem Eigenschaftenfeld angezeigt wird, wählen Sie darauf, um ein Generator anzuzeigen oder Anzeigen eines Dialogfelds bietet Ihnen eine Auswahl von Generatoren. Beispielsweise können Sie die Code-Generators, Makro-Generator oder Abfrage-Generator verwenden, um bestimmte Eigenschaften festzulegen.

## <a name="tips"></a>Tipps

- Microsoft Access stellt ein **Zoom** -Feld für die Eingabe und die Anzeige von Ausdrücken oder anderen langen Eigenschafteneinstellungen bereit. Um das Dialogfeld **Zoom** anzuzeigen, wählen Sie ein Eigenschaftenfeld im Eigenschaftenfenster. Drücken Sie UMSCHALT + F2 oder mit der rechten Maustaste, und wählen Sie dann im Kontextmenü auf **Zoom** .

- Sie können die Eigenschaft **Steuerelementinhalt** für einige Steuerelemente einstellen, indem Sie die Eigenschafteneinstellung im Steuerelement selbst vornehmen.

- Durch Ändern der Standardeigenschafteneinstellungen für einen Steuerelementtyp erreichen Sie, dass später von Ihnen erstellte Steuerelemente über die neuen Standardeinstellungen verfügen.

- Die Eigenschafteneinstellungen eines gebundenen Steuerelements stimmen nicht immer mit den entsprechenden Einstellungen im Feld der zugrunde liegenden Tabelle oder Abfrage überein, an die das Steuerelement gebunden ist. In diesem Fall setzen die Einstellungen des Formulars oder Berichts in der Regel die Einstellungen der Tabelle oder Abfrage außer Kraft.

