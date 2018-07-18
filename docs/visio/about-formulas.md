---
title: Informationen zu Formeln
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: Der Schlüssel zum Steuern von Shape-Aktionen ist das Erstellen von Formeln, die das von Ihnen gewünschte Verhalten definieren. Sie können die Formel einer Zelle umschreiben, um den Zellenwert und somit das Verhalten eines bestimmten Shapes zu ändern. Die Zelle Hight im Abschnitt Shape Transform enthält beispielsweise eine Formel, die Sie bearbeiten können, um die Höhe des Shapes zu ändern.
ms.openlocfilehash: 7df5ffe4d3dc32bcd5209bde353c39a92c7d422b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796351"
---
# <a name="about-formulas"></a><span data-ttu-id="48049-105">Informationen zu Formeln</span><span class="sxs-lookup"><span data-stu-id="48049-105">About Formulas</span></span>

<span data-ttu-id="48049-p102">Der Schlüssel zum Steuern von Shape-Aktionen ist das Erstellen von Formeln, die das von Ihnen gewünschte Verhalten definieren. Sie können die Formel einer Zelle umschreiben, um den Zellenwert und somit das Verhalten eines bestimmten Shapes zu ändern. Die Zelle Hight im Abschnitt Shape Transform enthält beispielsweise eine Formel, die Sie bearbeiten können, um die Höhe des Shapes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="48049-p102">The key to controlling shape actions is to write formulas that define the behavior you want. You can edit a cell's formula to change the value of the cell and, as a result, change a particular shape's behavior. For example, the Height cell in the Shape Transform section contains a formula that you can change to alter the shape's height.</span></span>
  
<span data-ttu-id="48049-p103">Microsoft Visio-Formeln ähneln in vielerlei Hinsicht typischen Formeln in einem Tabellenkalkulationsprogramm. Visio betrachtet den gesamten Zelleninhalt als Formel, auch wenn es sich um einen numerischen Wert oder eine einfache Zellenreferenz handelt.</span><span class="sxs-lookup"><span data-stu-id="48049-p103">Microsoft Visio formulas are similar to typical spreadsheet formulas in many ways. Visio regards anything in a cell, even if it is a numeric value or simple cell reference, as a formula.</span></span>
  
<span data-ttu-id="48049-p104">Eine Formel in einer Zelle kann aus der äquivalenten Zelle eines Masters oder einer Formatvorlage geerbt oder lokal definiert werden. Visio berechnet die Formel und wandelt die Ergebnisse anschließend in einen entsprechenden Wert mit entsprechenden Einheiten für die Zelle um. In einem ShapeSheet-Fenster können Sie Zelleninhalte entweder als Formeln oder Werte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="48049-p104">A formula in a cell can be inherited from the equivalent cell of a master or a style or defined locally. Visio evaluates the formula and then converts the results to an appropriate value and appropriate units for the cell. In a ShapeSheet window, you can display cell contents as either formulas or values.</span></span>
  
## <a name="elements-of-a-formula"></a><span data-ttu-id="48049-114">Elemente einer Formel</span><span class="sxs-lookup"><span data-stu-id="48049-114">Elements of a formula</span></span>

<span data-ttu-id="48049-p105">Eine Formel beginnt immer mit einem Gleichheitszeichen, das automatisch eingefügt wird, und kann jedes der folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="48049-p105">A formula always starts with an equal sign, which is inserted automatically. A formula can include any of the following elements:</span></span>
  
- <span data-ttu-id="48049-117">Zahlen</span><span class="sxs-lookup"><span data-stu-id="48049-117">Numbers</span></span>
    
- <span data-ttu-id="48049-118">Koordinaten</span><span class="sxs-lookup"><span data-stu-id="48049-118">Coordinates</span></span>
    
- <span data-ttu-id="48049-119">Boolesche Werte</span><span class="sxs-lookup"><span data-stu-id="48049-119">Boolean values</span></span>
    
- <span data-ttu-id="48049-120">Operatoren</span><span class="sxs-lookup"><span data-stu-id="48049-120">Operators</span></span>
    
- <span data-ttu-id="48049-121">Funktionen</span><span class="sxs-lookup"><span data-stu-id="48049-121">Functions</span></span>
    
- <span data-ttu-id="48049-122">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="48049-122">Strings</span></span>
    
- <span data-ttu-id="48049-123">Zellenreferenzen</span><span class="sxs-lookup"><span data-stu-id="48049-123">Cell references</span></span>
    
- <span data-ttu-id="48049-124">Maßeinheiten</span><span class="sxs-lookup"><span data-stu-id="48049-124">Units of measure</span></span>
    
## <a name="default-formulas"></a><span data-ttu-id="48049-125">Standardformeln</span><span class="sxs-lookup"><span data-stu-id="48049-125">Default formulas</span></span>

<span data-ttu-id="48049-p106">Wenn Sie ein Shape erstellen, erstellt Visio standardmäßig Formeln für das Shape. Um die standardmäßigen Formeln anzuzeigen, zeichnen Sie ein einfaches Shape (z. B. ein Rechteck, eine Ellipse oder eine gerade Linie), und öffnen Sie das ShapeSheet-Fenster (klicken Sie auf der Registerkarte [Entwickler](run-in-developer-mode-display-the-developer-tab.md) auf **ShapeSheet anzeigen**).</span><span class="sxs-lookup"><span data-stu-id="48049-p106">When you create a shape, Visio creates formulas for it by default. To see what the default formulas are, draw a simple shape (such as a rectangle, ellipse, or straight line) and open its ShapeSheet window (on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, click **Show ShapeSheet**).</span></span>
  
## <a name="inherited-formulas"></a><span data-ttu-id="48049-128">Geerbte Formeln</span><span class="sxs-lookup"><span data-stu-id="48049-128">Inherited formulas</span></span>

<span data-ttu-id="48049-p107">Visio vererbt Formeln, wann immer dies möglich ist. Anstatt eine lokale Kopie jeder Formel in der Instanz anzulegen, erbt eine Instanz Formeln aus ihrem Master in der Dokumentschablone und die Formatierung aus der zusammen mit der Zeichnung gespeicherten Formatvorlage. Dieses Verhalten führt zu kleineren Dateien, ermöglicht aber auch Änderungen an den Formeln des Masters oder an der Formatvorlage, die an alle Instanzen weitergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="48049-p107">Visio inherits formulas whenever possible. Rather than make a local copy of every formula in the instance, an instance inherits formulas from its master on the document stencil and inherits formatting from the style definition stored with the drawing. This behavior results in smaller files, but also allows changes to the master's formulas or the style definition to be propagated to all instances.</span></span>
  
<span data-ttu-id="48049-132">Schwarzer Text in einer Zelle weist auf eine geerbte Formel hin.</span><span class="sxs-lookup"><span data-stu-id="48049-132">Black text in a cell indicates an inherited formula.</span></span>
  
## <a name="local-formulas"></a><span data-ttu-id="48049-133">Lokale Formeln</span><span class="sxs-lookup"><span data-stu-id="48049-133">Local formulas</span></span>

<span data-ttu-id="48049-p108">Wenn Sie eine lokale Formel für eine Instanz schreiben, ersetzen Sie die geerbte Formel in der Zelle durch eine lokale Überschreibung. Zukünftige Änderungen an dieser Zelle im Master oder in der Formatvorlage haben keine Auswirkungen auf diese Instanz, da Vererbung für die Zelle mit der lokalen Überschreibung gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="48049-p108">When you write a local formula for an instance, you are replacing the inherited formula in the cell with a local override. Future changes to that cell in the master or style do not affect this instance because it has blocked inheritance for the cell with the local override.</span></span>
  
<span data-ttu-id="48049-136">Durch das Anwenden einer Formatvorlage werden sämtliche lokalen Formeln in den verwandten Zellen gelöscht, sofern Sie sie nicht die Funktion SCHÜTZEN verwenden, um sie zu schützen.</span><span class="sxs-lookup"><span data-stu-id="48049-136">Applying a style deletes all local formulas in the related cells unless you use the GUARD function to protect them.</span></span>
  
<span data-ttu-id="48049-137">Blauer Text weist auf eine lokale Formel hin, die entweder das Ergebnis einer im ShapeSheet-Fenster bearbeiteten Formel oder einer Änderung am Shape ist, die Visio dazu veranlasst hat, die Formel für diese Zelle zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="48049-137">Blue text indicates a local formula, either the result of editing the formula in a ShapeSheet window or some change to the shape that caused Visio to reset the formula for that cell.</span></span>
  
## <a name="automatic-updates-to-formulas"></a><span data-ttu-id="48049-138">Automatische Aktualisierungen von Formeln</span><span class="sxs-lookup"><span data-stu-id="48049-138">Automatic updates to formulas</span></span>

 <span data-ttu-id="48049-p109">Visio aktualisiert bestimmte Zellen automatisch, sobald Sie ein Shape in einer Zeichnung ändern. Dies bedeutet, dass unter bestimmten Umständen von Ihnen eingegebene Formeln ersetzt werden können. Wenn Sie beispielsweise an einem Eckpunkt ziehen, um die Größe eines Shapes zu ändern, setzt Visio die Formeln in den Zellen PinX, PinY, Width und Hight zurück.</span><span class="sxs-lookup"><span data-stu-id="48049-p109">Visio automatically updates certain cells whenever you change a shape in a drawing. This means that under some circumstances formulas you enter can be replaced. For example, if you drag a corner handle to resize a shape, Visio resets formulas in the PinX, PinY, Width, and Height cells.</span></span> 
  
<span data-ttu-id="48049-142">Sie können Formeln ggf. mithilfe der Funktion SCHÜTZEN vor Änderungen schützen.</span><span class="sxs-lookup"><span data-stu-id="48049-142">If necessary, you can protect formulas against changes by using the GUARD function.</span></span>
  

