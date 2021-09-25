---
title: Zeile "Connection Points" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3005
ms.localizationpriority: medium
ms.assetid: eaac62a5-f516-9b81-587a-8e0e02de59ee
description: Enthält die X- und Y-Koordinaten, die horizontale und vertikale Richtung sowie den Typ für einen einzelnen Verbindungspunkt in einem Shape. Koordinaten von Verbindungspunkten werden vom Ursprung des Shapes gemessen. Ein Shape enthält eine Verbindungspunktezeile für jeden Verbindungspunkt.
ms.openlocfilehash: 49596be9a713d48b6262edcf1a7c3d4f64a735bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582938"
---
# <a name="connection-points-row-connection-points-section"></a>Zeile "Connection Points" (Abschnitt "Connection Points")

Enthält die  *X-*  und  *Y-Koordinaten,*  die horizontale und vertikale Richtung sowie den Typ für einen einzelnen Verbindungspunkt in einem Shape. Koordinaten von Verbindungspunkten werden vom Ursprung des Shapes gemessen. Ein Shape enthält eine Verbindungspunktezeile für jeden Verbindungspunkt. 
  
Wenn Verbindungspunktezeilen benannt sind, werden diese Namen als Connections angezeigt. *Name*  im ShapeSheet-Fenster. Verbindungspunkte enthalten die folgenden Zellen. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |Die  x-Koordinate für einen Verbindungspunkt in lokalen Koordinaten.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |Die  y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |Die  *x-Komponente*  für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle akzeptiert einen Fließkommawert.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |Die  *y-Komponente*  für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle akzeptiert einen Fließkommawert.  <br/> |
|[Typ/C](typec-cell-connection-points-section.md) <br/> |Der Typ des Verbindungspunkts (0 = nach innen, 1 = nach außen, 2 = nach innen + nach außen).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann. Klicken Sie mit der rechten Maustaste auf eine Zeile, um auf diese Zelle zuzugreifen, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**.<br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Zellen in den Verbindungen. *Namenzeilen*  werden mit DirX/A, DirY/B und Typ/C bezeichnet, da diese Zeilen erweitert oder nicht erweitert werden können. 
  
Die meisten Verbindungspunkte (alle über die Benutzeroberfläche erstellten Verbindungspunkte) sind nicht erweitert und verfügen über DirX-, DirY- und Type-Zellen. Der Zeilentyp lautet **visTagCnnctPt** oder **visTagCnnctNamed.**
  
In nicht erweiterten Zeilen definieren die Zellen DirX und DirY gemeinsam einen Richtungsvektor, der die Drehung von Shapes beeinflusst, die in Verbindungen mithilfe des Verbindungspunkts verwendet werden. Wenn beide Null sind, ist der Punkt richtungslos. Verbindungspunkte sind in folgende Typen unterteilt:
  
- Nach innen (0). Dies bedeutet, dass Shapes an ihnen kleben. Dies ist die Standardeinstellung.
    
- Nach außen (1). Dies bedeutet, dass diese Verbindungspunkte an nach innen gerichteten Verbindungspunkten kleben.
    
- Nach innen und Nach außen (2). In diesem Fall ist der Verbindungspunkt nach innen gerichtet, und die entgegengesetzte Richtung gilt, wenn er als Verbindung nach außen verwendet wird.
    
Erweiterte Zeilen haben die Zellen A, B, C und D und verhalten sich wie richtungslose, nicht erweiterte Zeilen vom Typ "Nach innen". Erweiterte Zeilen werden nicht häufig verwendet, aber Sie können sie verwenden, um Daten einem Verbindungspunkt in den Zellen A, B, C und D zuzuordnen. Der Zeilentyp lautet **visTagCnnctPtABCD** oder **visTagCnnctNamedABCD.** Erweiterte Zeilen können durch das Vorhandensein einer Formel in der Zelle D identifiziert werden. 
  
 Sie können so viele Verbindungen hinzufügen.  *Benennen*  Sie Zeilen nach Bedarf, weisen Sie den Zeilen aussagekräftige Namen zu, und legen Sie Zellwerte fest. Um einem vorhandenen Abschnitt "Verbindungspunkte" einen Verbindungspunkt hinzuzufügen, klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **"Zeile einfügen".** 
  
Sie können auf Verbindungspunkte-Zeilenzellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. Klicken Sie zum Ändern des Zeilennamens darauf, und geben Sie einen Namen wie  *z. B. Custom*  ein, um den Zeilennamen Connections.Custom zu erstellen. Anschließend können Sie mit connections.Custom.X oder Connections.X1 auf die Zelle X verweisen, wenn Sie die Zeilennummer verwenden möchten. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein. Wenn Sie einen Namen für eine Zeile im Abschnitt "Verbindungspunkte" erstellen, Microsoft Office Visio alle Zeilen im Abschnitt mit dem Standardnamen Connections.Row_ *n benennt.* 
  
Benannte Zeilen Connection Points sind mit Versionen von Visio vor Version 5.0 nicht kompatibel. Wenn eine Visio-Zeichnungsdatei mit benannten Zeilen Verbindungspunkte in einem älteren Format gespeichert wird, werden Verweise auf benannte Zeilen Connection Points in indizierte Verweise konvertiert, und die Zeilennamen gehen verloren.
  

