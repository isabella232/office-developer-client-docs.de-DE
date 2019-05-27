---
title: Festlegen von Formular-, Berichts- und Steuerelementeigenschaften
TOCTitle: Set form, report, and control properties
description: Jedes Formular, jeder Bericht, jeder Bereich und jedes Steuerelement verfügt über Eigenschafteneinstellungen, mit denen Sie das Aussehen und die Funktionsweise eines Elements in Access 2013 ändern können.
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308736"
---
# <a name="set-form-report-and-control-properties"></a>Festlegen von Formular-, Berichts- und Steuerelementeigenschaften

**Gilt für**: Access 2013, Office 2013

Jedes Formular, jeder Bericht, jeder Bereich und jedes Steuerelement verfügt über Eigenschafteneinstellungen, mit denen Sie das Aussehen und die Funktionsweise eines Elements ändern können. Sie können die Eigenschaften im Eigenschaftenfenster, in einem Makro oder in Visual Basic anzeigen und ändern.

## <a name="set-properties"></a>Festlegen von Eigenschaften

1. Wählen Sie in der Formularentwurfsansicht oder Berichtsentwurfsansicht das Steuerelement, den Bereich, das Formular oder den Bericht aus, für das bzw. den Sie die Eigenschaft einstellen möchten. Sie haben folgende Auswahlmöglichkeiten:
    
   - Ein oder mehrere Steuerelemente. Wenn Sie mehrere Steuerelemente auswählen möchten, klicken Sie bei gedrückter UMSCHALTTASTE auf die gewünschten Steuerelemente, oder ziehen Sie den Mauszeiger über die gewünschten Steuerelemente. Wenn Sie mehrere Steuerelemente auswählen, zeigt das Eigenschaftenfenster nur die Eigenschaften an, die alle markierten Steuerelemente gemeinsam besitzen.
    
   - Einen Bereich. Klicken Sie auf den Bereichsmarkierer des gewünschten Bereichs.
    
   - Das gesamte Formular oder den gesamten Bericht. Klicken Sie auf den Formularmarkierer oder Berichtsmarkierer in der oberen linken Ecke des Formulars bzw. Berichts.

2. Zeigen Sie das Eigenschaftenfenster an, indem Sie zuerst mit der rechten Maustaste auf das Objekt oder den Bereich und dann im Kontextmenü auf **Eigenschaften** klicken, oder indem Sie auf der Symbolleiste auf **Eigenschaften** klicken.

3. Klicken Sie auf die Eigenschaft, deren Wert Sie festlegen möchten, und führen Sie dann einen der folgenden Schritte durch:
    
   - Geben Sie im Eigenschaftenfeld die entsprechende Einstellung oder den entsprechenden Ausdruck an.
    
   - Wenn das Einstellungsfeld der Eigenschaft einen Pfeil enthält, klicken Sie auf den Pfeil, und klicken Sie dann in der Liste auf einen Wert.
    
   - Wenn eine **Build**-Schaltfläche rechts neben dem Eigenschaftenfeld angezeigt wird, wählen Sie diese aus, um einen Generator oder ein Dialogfeld anzuzeigen, in dem Sie eine Auswahl von Generatoren finden. Sie können z. B. den Code-Generator, den Makro-Generator oder den Abfrage-Generator verwenden, um einige Eigenschaften festzulegen.

## <a name="tips"></a>Tipps 

- Microsoft Access bietet ein **Zoom**-Feld, in dem Sie Ausdrücke oder andere Eigenschafteneinstellungen eingeben oder anzeigen können. Um das **Zoom**-Feld anzuzeigen, klicken Sie im Eigenschaftenfenster auf das Eigenschaftenfeld. Drücken Sie UMSCHALT+F2, oder klicken Sie zuerst mit der rechten Maustaste, und klicken Sie dann im Kontextmenü auf **Zoom**.

- Sie können die Eigenschaft **Steuerelementinhalt** für einige Steuerelemente einstellen, indem Sie die Eigenschafteneinstellung im Steuerelement selbst vornehmen.

- Durch Ändern der Standardeigenschafteneinstellungen für einen Steuerelementtyp erreichen Sie, dass später von Ihnen erstellte Steuerelemente über die neuen Standardeinstellungen verfügen.

- Die Eigenschafteneinstellungen eines gebundenen Steuerelements stimmen nicht immer mit den entsprechenden Einstellungen im Feld der zugrunde liegenden Tabelle oder Abfrage überein, an die das Steuerelement gebunden ist. In diesem Fall setzen die Einstellungen des Formulars oder Berichts in der Regel die Einstellungen der Tabelle oder Abfrage außer Kraft.

