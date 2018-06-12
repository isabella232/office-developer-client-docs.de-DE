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
# <a name="about-formulas"></a>Informationen zu Formeln

Der Schlüssel zum Steuern von Shape-Aktionen ist das Erstellen von Formeln, die das von Ihnen gewünschte Verhalten definieren. Sie können die Formel einer Zelle umschreiben, um den Zellenwert und somit das Verhalten eines bestimmten Shapes zu ändern. Die Zelle Hight im Abschnitt Shape Transform enthält beispielsweise eine Formel, die Sie bearbeiten können, um die Höhe des Shapes zu ändern.
  
Microsoft Visio-Formeln ähneln in vielerlei Hinsicht typischen Formeln in einem Tabellenkalkulationsprogramm. Visio betrachtet den gesamten Zelleninhalt als Formel, auch wenn es sich um einen numerischen Wert oder eine einfache Zellenreferenz handelt.
  
Eine Formel in einer Zelle kann aus der äquivalenten Zelle eines Masters oder einer Formatvorlage geerbt oder lokal definiert werden. Visio berechnet die Formel und wandelt die Ergebnisse anschließend in einen entsprechenden Wert mit entsprechenden Einheiten für die Zelle um. In einem ShapeSheet-Fenster können Sie Zelleninhalte entweder als Formeln oder Werte anzeigen.
  
## <a name="elements-of-a-formula"></a>Elemente einer Formel

Eine Formel beginnt immer mit einem Gleichheitszeichen, das automatisch eingefügt wird, und kann jedes der folgenden Elemente enthalten.
  
- Zahlen
    
- Koordinaten
    
- Boolesche Werte
    
- Operatoren
    
- Funktionen
    
- Zeichenfolgen
    
- Zellenreferenzen
    
- Maßeinheiten
    
## <a name="default-formulas"></a>Standardformeln

Wenn Sie ein Shape erstellen, erstellt Visio Formeln für standardmäßig an. Um herauszufinden, was die standardmäßigen Formeln sind, zeichnen Sie eine einfache Form (beispielsweise ein Rechteck, eine Ellipse oder ein gerader Linie), und öffnen Sie das ShapeSheet-Fenster (klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) auf **ShapeSheet anzeigen**).
  
## <a name="inherited-formulas"></a>Geerbte Formeln

Visio vererbt Formeln, wann immer dies möglich ist. Anstatt eine lokale Kopie jeder Formel in der Instanz anzulegen, erbt eine Instanz Formeln aus ihrem Master in der Dokumentschablone und die Formatierung aus der zusammen mit der Zeichnung gespeicherten Formatvorlage. Dieses Verhalten führt zu kleineren Dateien, ermöglicht aber auch Änderungen an den Formeln des Masters oder an der Formatvorlage, die an alle Instanzen weitergegeben werden sollen.
  
Schwarzer Text in einer Zelle weist auf eine geerbte Formel hin.
  
## <a name="local-formulas"></a>Lokale Formeln

Wenn Sie eine lokale Formel für eine Instanz schreiben, ersetzen Sie die geerbte Formel in der Zelle durch eine lokale Überschreibung. Zukünftige Änderungen an dieser Zelle im Master oder in der Formatvorlage haben keine Auswirkungen auf diese Instanz, da Vererbung für die Zelle mit der lokalen Überschreibung gesperrt ist.
  
Durch das Anwenden einer Formatvorlage werden sämtliche lokalen Formeln in den verwandten Zellen gelöscht, sofern Sie sie nicht die Funktion SCHÜTZEN verwenden, um sie zu schützen.
  
Blauer Text weist auf eine lokale Formel hin, die entweder das Ergebnis einer im ShapeSheet-Fenster bearbeiteten Formel oder einer Änderung am Shape ist, die Visio dazu veranlasst hat, die Formel für diese Zelle zurückzusetzen.
  
## <a name="automatic-updates-to-formulas"></a>Automatische Aktualisierungen von Formeln

 Visio aktualisiert bestimmte Zellen automatisch, sobald Sie ein Shape in einer Zeichnung ändern. Dies bedeutet, dass unter bestimmten Umständen von Ihnen eingegebene Formeln ersetzt werden können. Wenn Sie beispielsweise an einem Eckpunkt ziehen, um die Größe eines Shapes zu ändern, setzt Visio die Formeln in den Zellen PinX, PinY, Width und Hight zurück. 
  
Sie können Formeln ggf. mithilfe der Funktion SCHÜTZEN vor Änderungen schützen.
  

