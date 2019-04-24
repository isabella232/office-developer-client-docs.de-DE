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
description: Enthält die x-und y-Koordinaten, die horizontale und die vertikale Richtung und den Typ für einen einzelnen Verbindungspunkt in einem Shape. Koordinaten der Verbindungspunkte werden vom Ursprung der Form gemessen. Ein Shape enthält für jeden Verbindungspunkt eine Zeile mit Verbindungspunkten.
ms.openlocfilehash: 301ea4fb446d9acafd4b59af388c3e7b2d419e20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361026"
---
# <a name="connection-points-row-connection-points-section"></a>Zeile "Connection Points" (Abschnitt "Connection Points")

Enthält die *x* -und *y* -Koordinaten, die horizontale und die vertikale Richtung und den Typ für einen einzelnen Verbindungspunkt in einem Shape. Koordinaten der Verbindungspunkte werden vom Ursprung der Form gemessen. Ein Shape enthält für jeden Verbindungspunkt eine Zeile mit Verbindungspunkten. 
  
Wenn Verbindungspunkt Zeilen benannt werden, werden diese Namen als Verbindungen angezeigt. *Name* im ShapeSheet-Fenster. Connection Points-Zeilen enthalten die folgenden Zellen. Weitere Informationen finden Sie in den Themen zu bestimmten Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |Die *x* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten.  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |Die *y* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten.  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |Die *x* -Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle akzeptiert einen Fließkommawert.  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |Die *y* -Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle akzeptiert einen Fließkommawert.  <br/> |
|[Typ/C](typec-cell-connection-points-section.md) <br/> |Der Typ des Verbindungspunkts (0 = nach innen, 1 = nach außen, 2 = nach innen + nach außen).  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |Eine Zelle für den Entwurf, die zum Eingeben oder Testen von Formeln verwendet werden kann. Klicken Sie mit der rechten Maustaste auf eine Zeile, um auf diese Zelle zuzugreifen, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**.<br/> |
   
## <a name="remarks"></a>Bemerkungen

Zellen in den Verbindungen. die Zeile *Name heißt* DirX/A, DirY/B und Type/C, da es sich bei diesen Zeilen um erweiterte oder nicht erweiterte Zeilen handeln kann. 
  
Die meisten Verbindungspunkte (alle Verbindungspunkte, die über die Benutzeroberfläche erstellt werden) sind nicht erweitert und verfügen über DirX-, DirY-und Type-Zellen. Der Zeilentyp ist **visTagCnnctPt** oder **visTagCnnctNamed.**
  
In nicht erweiterten Zeilen definieren die Zellen DirX und DirY gemeinsam einen Richtungsvektor, der die Drehung von Shapes beeinflusst, die in Verbindungen mithilfe des Verbindungspunkts verwendet werden. Wenn beide Null sind, ist der Punkt richtungslos. Verbindungspunkte sind in folgende Typen unterteilt:
  
- Nach innen (0). Dies bedeutet, dass Shapes an ihnen kleben. Dies ist die Standardeinstellung.
    
- Nach außen (1). Dies bedeutet, dass diese Verbindungspunkte an nach innen gerichteten Verbindungspunkten kleben.
    
- Nach innen und Nach außen (2). In diesem Fall ist der Verbindungspunkt nach innen gerichtet, und die entgegengesetzte Richtung gilt, wenn er als Verbindung nach außen verwendet wird.
    
Erweiterte Zeilen haben die Zellen A, B, C und D und Verhalten sich wie richtungsfreie, nicht erweiterte Zeilen vom Typ nach innen. Erweiterte Zeilen werden nicht häufig verwendet, aber Sie können Sie verwenden, um Daten mit einem Verbindungspunkt in den Zellen A, B, C und D zu verknüpfen. Der Zeilentyp ist **visTagCnnctPtABCD** oder **visTagCnnctNamedABCD**. Erweiterte Zeilen können durch das vorhanden sein einer Formel in der Zelle D identifiziert werden. 
  
 Sie können so viele Verbindungen hinzufügen.  *benennen* Sie Zeilen, die Sie benötigen, und weisen Sie den Zeilen aussagekräftige Namen zu. Klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **Zeile einfügen** , um einen Verbindungspunkt zu einem vorhandenen Connection Points-Abschnitt hinzuzufügen. 
  
Sie können auf Verbindungspunkt Zeilen Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. Um den Zeilennamen zu ändern, klicken Sie darauf, und geben Sie dann einen Namen wie *Custom* ein, um beispielsweise den Zeilennamen Connections. Custom zu erstellen. Sie können dann mithilfe von Connections. Custom. X, beispielsweise oder Connections. x1 auf die Zelle X verweisen, wenn Sie die Zeilennummer verwenden möchten. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein. Wenn Sie im Abschnitt Connection Points einen Namen für eine Zeile erstellen, benennt Microsoft Office Visio alle Zeilen im Abschnitt mit dem Standardnamen Connections. Row_ *n* . 
  
Benannte Zeilen Connection Points sind mit Versionen von Visio vor Version 5.0 nicht kompatibel. Wenn eine Visio-Zeichnungsdatei mit benannten Zeilen Verbindungspunkte in einem älteren Format gespeichert wird, werden Verweise auf benannte Zeilen Connection Points in indizierte Verweise konvertiert, und die Zeilennamen gehen verloren.
  

