---
title: Informationen zur ShapeSheet-Kalkulationstabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251822
localization_priority: Normal
ms.assetid: f403890d-4a3a-bacc-53d7-1b9920b23639
description: Jedem Objekt in Microsoft Visio (Dokument, Zeichenblatt, Formatvorlage, Shape, Gruppe, Shape oder Objekt in einer Gruppe, Master-Shape, Objekt aus einem anderen Programm, Führungslinie und Führungspunkt) ist eine ShapeSheet-Kalkulationstabelle zugeordnet, in der wichtige objektspezifische Informationen aufgeführt sind. Diese Kalkulationstabelle enthält Informationen wie Höhe, Breite, Winkel, Farbe sowie andere Attribute, die das Erscheinungsbild und das Verhalten des Shapes definieren.
ms.openlocfilehash: f443a596174ac4a555d53a271372e73367197da0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796359"
---
# <a name="about-the-shapesheet-spreadsheet"></a>Informationen zur ShapeSheet-Kalkulationstabelle

Jedem Objekt in Microsoft Visio (Dokument, Zeichenblatt, Formatvorlage, Shape, Gruppe, Shape oder Objekt in einer Gruppe, Master-Shape, Objekt aus einem anderen Programm, Führungslinie und Führungspunkt) ist eine ShapeSheet-Kalkulationstabelle zugeordnet, in der wichtige objektspezifische Informationen aufgeführt sind. Diese Kalkulationstabelle enthält Informationen wie Höhe, Breite, Winkel, Farbe sowie andere Attribute, die das Erscheinungsbild und das Verhalten des Shapes definieren.
  
Als Shape-Entwickler müssen Sie das Erscheinungsbild und Verhalten der von Ihnen erstellten Shapes ohne Einschränkungen und genauestens steuern können. Sie können das Standardverhalten eines Shapes ändern sowie seine Funktionalität erweitern, indem Sie es über seine ShapeSheet-Kalkulationstabelle bearbeiten. Auf diese Tabelle können Sie in einem ShapeSheet-Fenster oder programmgesteuert zugreifen.
  
## <a name="viewing-an-object-in-a-shapesheet-window"></a>Anzeigen eines Objekts in einem ShapeSheet-Fenster

Das Visio-Zeichnungsfenster und das ShapeSheet-Fenster stellen verschiedene Ansichten desselben Shapes dar.
  
- Wenn Sie ein Shape in einem Zeichnungsfenster anzeigen, wird es grafisch gerendert angezeigt. Darüber hinaus verhält es sich gemäß den Formeln, die in seiner ShapeSheet-Kalkulationstabelle definiert sind.
    
- Wenn Sie ein Shape in einem ShapeSheet-Fenster anzeigen, sehen Sie die zugrunde liegenden Formeln, die bestimmen, wie das Shape auf dem Zeichenblatt angezeigt wird und wie es sich verhält.
    
Sie können ein ShapeSheet-Fenster und ein Zeichnungsfenster gleichzeitig anzeigen und sehen, wie das Shape im Zeichnungsfenster geändert wird, während Sie Zellen im entsprechenden ShapeSheet-Fenster ändern bzw. umgekehrt. Wenn Sie das Shape beispielsweise mit dem Mauszeiger verschieben, ändern sich die Formeln für PinX und PinY im Abschnitt Shape Transform, um die neue Position des Shapes auf dem Zeichenblatt anzuzeigen.
  
## <a name="structure-of-the-shapesheet-window"></a>Struktur des ShapeSheet-Fensters

Ein ShapeSheet ist unterteilt in *Abschnitte* , die einen bestimmten Aspekt der Verhalten eines Shapes oder die Darstellungsweise, steuern beispielsweise Geometrie oder Formatierung. Jeder Abschnitt enthält eine oder mehrere *Zeilen* , die *Zellen* enthalten. Jede Zelle kann eine Formel, dessen Ergebnis (häufig als der Wert der Zelle bezeichnet) und optionale Fehlerinformationen enthalten. Eine Formel, die möglicherweise erforderlich oder optional, je nach der jeweiligen Zelle. Eine Zelle Daten (beispielsweise die Formel oder Wert) können lokal definiert oder häufiger aus der entsprechenden Zelle in der Form Master oder einer Formatvorlage geerbt. 
  
Im folgenden Beispiel werden die Formelleiste ![Nummer 1](media/callout1_ZA01036259.gif), ein Abschnitt ![Nummer 2](media/callout2_ZA01036260.gif), eine Zelle ![Nummer 3](media/callout3_ZA01036261.gif)und eine Zeile ![Nummer 4](media/callout4_ZA01036262.gif) im ShapeSheet-Fenster veranschaulicht. 
  
![](media/ShpSheetRef_CA_02a_ZA07645861.gif)
  
Wenn Sie ein Shape zeichnen, zeichnet Visio das Shape als eine Auflistung der horizontalen und vertikalen Speicherorte mit Liniensegmenten verbunden. Diese Positionen (auch Scheitelpunkte genannt) werden in die Zellen X und Y die Shape- **Geometrie** -Abschnitt gespeichert. Wie im folgenden Beispiel angezeigt, wenn Sie die Zellen X und Y im Abschnitt **Geometry** des ShapeSheet-Fenster für ein Shape klicken, wird ein Schwarz versehen Feld Hervorhebung des Scheitelpunkts auf dem Shape im Zeichnungsfenster angezeigt. 
  
![](media/ShpSheetRef_CA_01_ZA07645860.gif)
  
## <a name="editing-an-object-in-the-shapesheet-window"></a>Bearbeiten eines Objekts im ShapeSheet-Fenster

Wenn ein ShapeSheet-Fenster aktiv ist, ändert sich das Menüband entsprechend, um Optionen für das Arbeiten in diesem Fenster anzuzeigen. Wenn Sie eine ShapeSheet-Zelle auswählen, wird eine Formelleiste angezeigt, die Sie verwenden können, um die Formeln eines Objekts einzugeben oder zu ändern. Sie können aber auch direkt in der Zelle arbeiten.
  
In einem ShapeSheet-Fenster können Sie die Abschnitte zu einer Form hinzu, um die neue Eigenschaften mit dem Shape auf dem Zeichenblatt hinzufügen hinzufügen. Beispielsweise können Sie einen Abschnitt **Connection Points** zum Erstellen einer Verbindung hinzufügen. Wenn Sie einen Abschnitt nicht mehr benötigen, können Sie ihn löschen. 
  
Sie können Zeilen auch Abschnitten zusätzliche Formeln zu speichern oder zum Ändern der Darstellung eines Shapes hinzufügen. Beispielsweise können Sie eine Zeile zu einem **Geometrie** -Abschnitt ein Segment mit einer Form hinzufügen hinzufügen. In ähnlicher Weise können Sie Zeilen löschen, die Sie nicht mehr benötigen. 
  
Sie können in Zellen entweder Formeln oder Werte anzeigen. Zeigen Sie Formeln an, wenn Sie neue Formeln eingeben, vorhandene Formeln ändern oder überprüfen möchten, in welcher Beziehung Formeln in verschiedenen Zellen zueinander stehen. Ein Wert ist das Ergebnis, das Sie erhalten, wenn Visio die Formel in einer Zelle berechnet. Sie können die Werte in den Zellen anzeigen, um die Ergebnisse der Berechnungen zu erhalten.
  
## <a name="additional-shapesheet-references"></a>Weitere Informationen zu ShapeSheets

Details zu einer bestimmten Abschnitt, eine Zeile oder eine Zelle im ShapeSheet finden Sie entsprechenden Artikel in dieser [ShapeSheet-Referenz](reference-visio-shapesheet.md).
  
Einzelheiten zum programmgesteuerten Zugriff auf die ShapeSheet-Kalkulationstabelle finden Sie in der Microsoft Visio Automation Reference.
  

