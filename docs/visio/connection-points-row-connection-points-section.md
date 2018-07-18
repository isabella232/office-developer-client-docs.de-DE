---
title: Zeile "Connection Points" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3005
localization_priority: Normal
ms.assetid: eaac62a5-f516-9b81-587a-8e0e02de59ee
description: Enthält die X- und y-Koordinaten, horizontalen und vertikalen Richtung und den Typ für eine einzelne Verbindung, zeigen Sie auf ein Shape. Koordinaten von Verbindungspunkten werden vom Ursprung des Shapes gemessen. Ein Shape enthält eine Zeile Connection Points für jeden Verbindungspunkt.
ms.openlocfilehash: f1b8daf7f9845b85e76020c7f89c8c42b4500823
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796716"
---
# <a name="connection-points-row-connection-points-section"></a>Connection Points Row (Connection Points Section)

Enthält die *X* - und *y* -Koordinaten, horizontalen und vertikalen Richtung und den Typ für eine einzelne Verbindung, zeigen Sie auf ein Shape. Koordinaten von Verbindungspunkten werden vom Ursprung des Shapes gemessen. Ein Shape enthält eine Zeile Connection Points für jeden Verbindungspunkt. 
  
Wenn Verbindungspunktzeilen benannt sind, werden diese Namen als Verbindungen angezeigt. *Name* im ShapeSheet-Fenster. Verbindungspunktzeilen enthält folgenden Zellen. Weitere Informationen finden Sie unter die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |Die *X* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |Die *y* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |Die *X* -Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Es wird auch zum Ausrichten des verbundenen Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle benötigt einen Gleitkommawert Codepunktwert.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |Die *y* -Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Es wird auch zum Ausrichten des verbundenen Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle benötigt einen Gleitkommawert Codepunktwert.  <br/> |
|[Type/C](typec-cell-connection-points-section.md) <br/> |Der Typ des Verbindungspunkts (0 = nach innen, 1 = nach außen, 2 = nach innen + nach außen).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann. Klicken Sie mit der rechten Maustaste auf eine Zeile, um auf diese Zelle zuzugreifen, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**.<br/> |
   
## <a name="remarks"></a>Bemerkungen

Zellen im Verbindungen. Zeile *Name* heißen DirX/A, DirY/B und Type/C, da diese Zeilen erweiterte oder nicht erweiterte Zeilen werden können. 
  
Die meisten Verbindungspunkte (alle Verbindungspunkte, die über die Benutzeroberfläche erstellt werden) sind nicht erweitert und besitzen DirX-, DirY- und Type-Zellen. Ihr Zeilentyp lautet visTagCnnctPt oder visTagCnnctNamed.
  
In nicht erweiterten Zeilen definieren die Zellen DirX und DirY gemeinsam einen Richtungsvektor, der die Drehung von Shapes beeinflusst, die in Verbindungen mithilfe des Verbindungspunkts verwendet werden. Wenn beide Null sind, ist der Punkt richtungslos. Verbindungspunkte sind in folgende Typen unterteilt:
  
- Nach innen (0). Dies bedeutet, dass Shapes an ihnen kleben. Dies ist die Standardeinstellung.
    
- Nach außen (1). Dies bedeutet, dass diese Verbindungspunkte an nach innen gerichteten Verbindungspunkten kleben.
    
- Nach innen und Nach außen (2). In diesem Fall ist der Verbindungspunkt nach innen gerichtet, und die entgegengesetzte Richtung gilt, wenn er als Verbindung nach außen verwendet wird.
    
Erweiterte Zeilen haben A-, B-, C- und D-Zellen und verhalten sich wie richtungslose, nicht erweiterte Zeilen vom Typ Nach innen. Erweiterte Zeilen werden nicht sehr häufig verwendet, doch Sie können sie verwenden, um Daten einem Verbindungspunkt in den A-, B-, C- und D-Zellen zuzuordnen. Ihr Zeilentyp ist visTagCnnctPtABCD oder visTagCnnctNamedABCD. Erweiterte Zeilen können dadurch identifiziert werden, dass eine Formel in der D-Zelle vorhanden ist. 
  
 Sie können beliebig viele Verbindungen hinzufügen.  *Namen* Zeilen wie Sie benötigen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen. Um einen vorhandenen Abschnitt Connection Points hinzufügen möchten, mit der rechten Maustaste in einer Zeile, und klicken Sie im Kontextmenü auf **Zeile einfügen** . 
  
Sie können Verbindungspunkte Zeilenzellen anhand ihrer Zeilennamen verweisen, die in einem ShapeSheet-Fenster als roter Text angezeigt. Um die Zeile mit dem Namen zu ändern, klicken Sie darauf, und geben Sie einen Namen wie beispielsweise *benutzerdefinierte* , beispielsweise, um den Zeilennamen Connections.Custom zu erstellen. Sie können dann verweisen die Zelle X mit Connections.Custom.X, oder Connections.X1, wenn Sie die Zeilennummer verwenden möchten. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein. Wenn Sie einen Namen für eine Zeile in den Abschnitt Connection Points erstellen, benennt Microsoft Office Visio alle Zeilen im Abschnitt mit den Standardnamen Row_ *n* . 
  
Benannte Zeilen Connection Points sind mit Versionen von Visio vor Version 5.0 nicht kompatibel. Wenn eine Visio-Zeichnungsdatei mit benannten Zeilen Verbindungspunkte in einem älteren Format gespeichert wird, werden Verweise auf benannte Zeilen Connection Points in indizierte Verweise konvertiert, und die Zeilennamen gehen verloren.
  

