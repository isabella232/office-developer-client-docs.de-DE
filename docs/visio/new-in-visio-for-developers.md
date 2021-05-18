---
title: New in Visio for developers
manager: soliver
ms.date: 09/18/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7e3fb858-0ab8-bd2e-217c-c85b10d79785
description: Dieses Dokument bietet eine Ansicht auf oberster Ebene der Verbesserungen und Ergänzungen für Entwickler in Visio 2013. Für Entwickler, die bereit sind, einen Sprung auf der Visio-Plattform zu starten, bietet es Ihnen genügend Details, um mit der Codierung für Visio 2013 zu beginnen.
ms.openlocfilehash: df4bc1fa493ee3976c99802400ee52691d05d20a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319817"
---
# <a name="new-in-visio-for-developers"></a>New in Visio for developers

Dieses Dokument bietet eine Ansicht auf oberster Ebene der Verbesserungen und Ergänzungen für Entwickler in Visio 2013. Für Entwickler, die bereit sind, einen Sprung auf der Visio-Plattform zu starten, bietet es Ihnen genügend Details, um mit der Codierung für Visio 2013 zu beginnen.
  
## <a name="introduction"></a>Einführung
<a name="vis15_WhatsNew_Intro"> </a>

Visio 2013 bietet eine leistungsstarke plattform für Ihre benutzerdefinierten Zeichnungslösungen. Neue Objekte, Sammlungen, Eigenschaften, Methoden, Aufzählungen und Ereignisse sowie neue ShapeSheet-Zellen und -Funktionen stellen Ihnen mehr Optionen für das Definieren des Verhaltens der Elemente in Ihren Lösungen bereit.
  
Zu den neuen Features, die Entwicklern in Visio 2013 interessieren, gehören das neue Dateiformat; robuste Updates für Designs; Ändern des Shape-Features (sodass Sie Formen durch ein anderes ersetzen können); neue Formeffekte; Verbesserungen beim Kommentieren; coauthoring on SharePoint Server 2013; anpassbare Bildausschnitte; relative Geometrie; Unterstützung für Business Connectivity Services (BCS)-Daten; updates to Visio Services in Microsoft SharePoint Server 2013; und ein duplikates Seitenfeature. Dieses Thema enthält eine kurze Zusammenfassung der einzelnen Features und enthält einige der neuen Visio-Objekte und Member, die den Features zugeordnet sind und in Visual Basic for Applications (VBA) verfügbar gemacht werden. Informationen zu diesen Features und zugehörigen Codebeispielen finden Sie [im Visio Developer Center](https://msdn.microsoft.com/office/aa905478.aspx).
  
> [!NOTE]
> Visio 2013 enthält viele neue ShapeSheet-Zellen, Zeilen und Funktionen zur Unterstützung der neuen Features in Visio. Weitere Informationen zu den neuen Informationen im ShapeSheet für Visio 2013 finden Sie im Artikel [What's new for Visio ShapeSheet developers](what-s-new-for-visio-shapesheet-developers.md). 
  
## <a name="new-file-format"></a>Neues Dateiformat
<a name="vis15_WhatsNew_NewFF"> </a>

Mit Visio 2013 wird ein neues Dateiformat eingeführt, das auf dem Open Packaging Conventions (OPC)-Standard (ISO 29500, Teil 2) und den XML-Elementen des vorherigen Visio-XML-Dateiformats (.vdx) basiert. Es handelt sich um ein komprimiertes, XML-basiertes Dateiformat, ähnlich wie bei anderen -Anwendungen.
  
Da das neue Dateiformat sowohl von Visio 2013 als auch von Visio Services in Microsoft SharePoint Server 2013 unterstützt wird, können Sie eine Visio-Zeichnung direkt in einer SharePoint Server-Bibliothek speichern, ohne die Datei als Visio-Webzeichnung (VDW) veröffentlichen zu müssen. Dennoch kann Visio Services Visio-Webzeichnungen weiterhin lesen und anzeigen.
  
Das neue Dateiformat enthält die folgenden Dateitypen (nach Erweiterung):
  
- .vsdx (Visio-Zeichnung)
    
- .vsdm (Visio-Zeichnung mit Makros)
    
- vssx (Visio-Schablone)
    
- .vsdm (Visio-Schablone mit Makros)
    
- vstx (Visio-Vorlage)
    
- .vstm (Visio-Vorlage mit Makros)
    
Mithilfe vorhandener Unterstützung für das Lesen und Schreiben in das Dateiformatpaket (z. B. [System.IO.Packaging)](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) und für die Analyse von XML ( [System.Xml. Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) ), können Sie programmgesteuert mit den neuen Dateiformaten arbeiten. 
  
Visio 2013 behält die Möglichkeit zum Lesen der alten Dateiformate (VSD, VSS, VST, VDX, VSX, VTX, VDW, VWI) bei. Visio 2013 wird nicht im vorherigen Visio -XML-Dateiformat (VDX) gespeichert. Lösungen oder Tools, die die vorherigen Visio XML-Dateiformatdateien (VDX) verwenden, müssen möglicherweise umgestaltet werden, um das neue Dateiformat und seine Schemas zu lesen.
  
Mit Visio Services können Visio-Webzeichnungen im Format VDW weiterhin im Browser angezeigt werden. Es können außerdem die neuen Formate Visio-Zeichnung (VSDX) und Visio-Zeichnung mit Makros (VSDM) gerendert werden.
  
## <a name="themes"></a>Designs
<a name="vis15_WhatsNew_Themes"> </a>

Designs wurden in Visio 2013 neu gestaltet und nutzen eine größere Auswahl an Effekten und Formatvorlagen, einschließlich der Integration von Shape Art-Effekten. Benutzer können jetzt ein übergeordnetes Format wählen, indem sie ein Design anwenden, das Diagramm mit Designvarianten personalisieren und einzelne Shapes mithilfe von Schnellformatvorlagen hervorheben. ShapeSheet-Entwickler können diese Features in Verbindung mit neuen Funktionen und Zellen im ShapeSheet nutzen.
  
Sie können Designs auch auf den Objektebenen [Seite](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx), [Shape](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) und [Auswahl](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) bearbeiten. Neue APIs für das Arbeiten mit Designs umfassen z. B. die [Page.SetTheme](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx)-Methode, die [Page.SetThemeVariant](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx)-Methode, die [Shape.SetQuickStyle](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx)-Methode und die [Selection.SetQuickStyle](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx)-Methode. 
  
Eine detaillierte Liste der neuen APIs in Visio 2013 finden Sie im Abschnitt [Visio Objektmodelländerungen](#vis15_WhatsNew_NewOM) in diesem Artikel. Weitere Informationen zu den neuen ShapeSheet-Zellen in Visio 2013 finden Sie im Artikel [What's new for Visio ShapeSheet developers](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="change-shape"></a>Shape ändern
<a name="vis15_WhatsNew_ChangeShapes"> </a>

Visio 2013 enthält eine Shapeersetzungs-API, mit der Sie eine oder mehrere Shapes gegen eine andere Form austauschen können, die in einer Schablone enthalten ist, während einige der lokalen Werte aus der ursprünglichen Form beibehalten werden, z. B. die Formtextform, Die Formdaten oder die Formformatierung. Shape-Entwickler können die ShapeSheet-Einstellungen ihrer benutzerdefinierten Shapes aktualisieren, um das Verhalten des Features "Shape ändern" für ihre Shapes anzugeben. Zu den neuen APIs zählen die [Shape.ReplaceShapes](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx)- und die [Selection.ReplaceShapes](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx)-Methode sowie das [ReplaceShape](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx)-Ereignis. 
  
Eine detaillierte Liste der neuen APIs in Visio 2013 finden Sie im Abschnitt [Visio Objektmodelländerungen](#vis15_WhatsNew_NewOM) in diesem Artikel. Weitere Informationen zu den neuen ShapeSheet-Zellen in Visio 2013 finden Sie im Artikel [What's new for Visio ShapeSheet developers](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="shape-effects"></a>Formeffekte
<a name="vis15_WhatsNew_ShapeEffects"> </a>

Visio 2013 wurden neue Formeffekte wie Abschrägung, 3D-Drehung, Leuchten, Reflektion und Skizze hinzugefügt. Das ShapeSheet enthält neue Zellen für das Arbeiten mit diesen Effekten.
  
Weitere Informationen zu den neuen ShapeSheet-Zellen in Visio 2013 finden Sie im Artikel [What's new for Visio ShapeSheet developers](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="commenting"></a>Kommentare
<a name="vis15_WhatsNew_Commenting"> </a>

Visio 2013 enthält ein neues Framework für Kommentare. Kommentare können jetzt einer bestimmten Form oder Seite zugeordnet werden. Visio 2013 enthält zwei neue Objekte, [Comments](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) und [Comment](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx). Neue APIs für den programmgesteuerten Zugriff auf Kommentare enthalten die Eigenschaften [Document.Comments](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx), [Page.Comments](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx), [Shape.Comments](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) und [Page.ShapeComments](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx). 
  
Visio Dienste umfassen JavaScript-APIs zum Lesen der Kommentare von einer Seite oder Form in einem Diagramm.
  
Eine detaillierte Liste der neuen APIs in Visio 2013 finden Sie im Abschnitt [Visio Objektmodelländerungen](#vis15_WhatsNew_NewOM) in diesem Artikel. 
  
> [!NOTE]
> Der Zugriff auf Kommentare über das ShapeSheet ist nicht mehr möglich. 
  
## <a name="coauthoring"></a>Gemeinsame Dokumenterstellung
<a name="vis15_WhatsNew_Coauthoring"> </a>

Visio 2013 umfasst die Möglichkeit, Diagramme, die auf einem SharePoint oder Microsoft OneDrive. Entwickler haben Zugriff auf das [Document.AfterDocumentMerge](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx)-Ereignis, das Informationen über Diagrammänderungen zur Verfügung stellt, die durch gemeinsame Dokumenterstellung entstehen. Lösungsentwickler haben außerdem die Möglichkeit, die gemeinsame Dokumenterstellung entsprechend ihren individuellen Anforderungen zu deaktivieren, und zwar mithilfe der [NoCoauth](nocoauth-cell-document-properties-section.md)-Zelle im Document-ShapeSheet. 
  
Eine detaillierte Liste der neuen APIs in Visio 2013 finden Sie im Abschnitt [Visio Objektmodelländerungen](#vis15_WhatsNew_NewOM) in diesem Artikel. 
  
## <a name="customizable-image-clipping"></a>Anpassbares Zuschneiden von Bildern
<a name="vis15_WhatsNew_ClipImages"> </a>

Visio 2013 unterstützt die Definition eines Pfads für das benutzerdefinierte Zuschneiden von Bildern, um Bilder zu beliebigen Formen zuzuschneiden. Dadurch werden die Kapazitäten von Visio 2010 erweitert, die das rechteckige Zuschneiden von Bildern unterstützten. Diese Funktion steht im ShapeSheet über die [ClippingPath](clippingpath-cell-foreign-image-info-section.md)-Zelle im Abschnitt **Foreign Image Info** zur Verfügung. 
  
Weitere Informationen zu den neuen ShapeSheet-Zellen in Visio 2013 finden Sie im Artikel [What's new for Visio ShapeSheet developers](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="relative-geometries"></a>Relative Geometrien
<a name="vis15_WhatsNew_RelativeGeometry"> </a>

In früheren Versionen Visio Formgeometrie durch Formeln definiert, die von der Höhe oder Breite der Form abhängen. In Visio 2010 wurden beispielsweise die Scheitelpunkte vieler integrierter Visio-Shapes durch Multiplizieren der Höhe oder Breite der Form mit einer Konstanten definiert. Diese Shapes  hatten Geometry-Abschnitte, die [MoveTo-](moveto-row-geometry-section.md) oder [LineTo-Zeilen](lineto-row-geometry-section.md) (z. B.) mit Formeln wie und `Width*1` `Height*0` enthielten.
  
Unter Visio 2013 wird für ShapeSheet jetzt die relative Geometrie unterstützt. Shapeentwickler können jetzt relative Geometrien verwenden, um Geometrien als einfache Werte oder Formeln anzugeben, die automatisch mit der Höhe oder Breite multipliziert werden. Shape-Scheitelpunkte können jetzt mit Konstanten ausgedrückt werden, z. B. ohne dass Scheitelpunkte als Vielfache der Formbreite oder -höhe ausgedrückt werden müssen. Dies erleichtert Entwicklern das Erstellen von Shapes mit einer besseren Leistung und kleineren Dateigrößen. Neue Zeilen enthalten die [Zeilen RelMoveTo](relmoveto-row-geometry-section.md) und [RelLineTo,](rellineto-row-geometry-section.md) wobei die **X-** und **Y-Zellenwerte** automatisch mit der Breite oder Höhe der Form (bzw.) multipliziert werden. 
  
Weitere Informationen zu den neuen ShapeSheet-Zeilen in Visio 2013 finden Sie im Artikel [What's new for Visio ShapeSheet developers](what-s-new-for-visio-shapesheet-developers.md).
  
## <a name="support-for-business-connectivity-services-bcs-data"></a>Unterstützung für Business Connectivity Services (BCS)-Daten
<a name="vis15_WhatsNew_BCS"> </a>

Visio 2013-Diagramme können nun mit externen Listen auf SharePoint Server 2013-Servern verbunden werden. Eine externe Liste ist eine Inhaltsquelle außerhalb von SharePoint (z. B. eine SQL Server-Tabelle), die mithilfe von Microsoft Business Connectivity Services (BCS) mit einer SharePoint-Liste verbunden wurde. Mit Visio Services können Sie Visio-Diagramme bei Aktualisierung der Daten aktualisieren.
  
Weitere Informationen zu den Neuen in Visio Services finden Sie im Artikel [Visio Services in SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx). Weitere Informationen zu Business Connectivity Services (BCS) finden Sie [unter Business Connectivity Services in SharePoint 2013](https://msdn.microsoft.com/library/jj163782%28office.15%29.aspx).
  
## <a name="improvements-in-visio-services"></a>Verbesserungen bei Visio Services
<a name="vis15_WhatsNew_VisioServices"> </a>

Visio Die Dienste in Microsoft SharePoint Server 2013 enthalten viele Verbesserungen. Wie bereits erwähnt, unterstützt Visio Services das neue Visio (sowohl vsdx als auch VSDM). Visio Dienste haben die Datenaktualisierung und Neuberechnung erweitert, einschließlich der Möglichkeit, Formeln über ein gesamtes Diagramm neu zu berechnen. 
  
Weitere Informationen zu den Neuen in Visio Services finden Sie im Artikel [Visio Services in SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx).
  
## <a name="duplicate-page"></a>Duplizieren von Seiten
<a name="vis15_WhatsNew_DuplicatePage"> </a>

Sie können nun eine Seite und alle ihre Formen innerhalb desselben Dokuments in Visio 2013 kopieren. Entsprechend verfügt das **Page**-Objekt über eine neue Methode, [Duplicate](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx), die die Seite dupliziert und ein neues **Page**-Objekt zurückgibt. 
  
## <a name="visio-object-model-changes"></a>Visio objektmodelländerungen
<a name="vis15_WhatsNew_NewOM"> </a>

Neue Objekte, Eigenschaften, Methoden und Ereignisse wurden dem Visio-Objektmodell hinzugefügt, um Programmierbarkeitsunterstützung für neue Visio 2013-Features zu bieten. Darüber hinaus adressieren Objektmodellverbesserungen häufige Entwickleranforderungen für Änderungen an der Visio Plattform.
  
### <a name="new-members"></a>Neue Member

Die folgenden Elemente wurden vorhandenen Objekten im Visio hinzugefügt.
  
 **Tabelle 1. Verbesserungen des Visio-Objektmodells**
  
|**Objekt oder Auflistung**|**Neue Member**|
|:-----|:-----|
|[Application-Objekt (Visio)](https://msdn.microsoft.com/library/5b3c8939-793f-116f-11b8-1d4170d95a63%28Office.15%29.aspx) <br/> |[Application.AfterReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/b02de031-086a-41cc-d832-5434b8096444%28Office.15%29.aspx) <br/> |
||[Application.BeforeReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/fbf44569-0539-9292-ce20-1f9e34238b33%28Office.15%29.aspx) <br/> |
||[Application.QueryCancelReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/50c0f2a6-f534-f3af-7e83-c865abda8bf9%28Office.15%29.aspx) <br/> |
||[Application.ReplaceShapesCanceled Event (Visio)](https://msdn.microsoft.com/library/e8eecd64-e4bd-d2c4-b942-c5ff607a4121%28Office.15%29.aspx) <br/> |
|[ApplicationSettings-Objekt (Visio)](https://msdn.microsoft.com/library/f2e24211-ecc6-e0f5-4c00-fc50f98a3505%28Office.15%29.aspx) <br/> |[ApplicationSettings.EnterCommitsText Property (Visio)](https://msdn.microsoft.com/library/ba9ce9fa-d224-cdc3-668d-46c1849911c7%28Office.15%29.aspx) <br/> |
||[ApplicationSettings.SVGExportFormat Property (Visio)](https://msdn.microsoft.com/library/9e7ca1cb-5ace-b75b-0e59-61566b9a0169%28Office.15%29.aspx) <br/> |
|[Document-Objekt (Visio)](https://msdn.microsoft.com/library/21640062-13a2-a2b2-7c61-7e707671207c%28Office.15%29.aspx) <br/> |[Document.AfterDocumentMerge Event (Visio)](https://msdn.microsoft.com/library/50658da5-592a-4d16-908f-c6abe3050f09%28Office.15%29.aspx) <br/> |
||[Document.Comments Property (Visio)](https://msdn.microsoft.com/library/15a322ad-70eb-1487-701d-76e2fde73309%28Office.15%29.aspx) <br/> |
||[Document.CompatibilityMode Property (Visio)](https://msdn.microsoft.com/library/98fc00d3-5d2b-218e-9828-b5581ee7313d%28Office.15%29.aspx) <br/> |
|[Documents-Objekt (Visio)](https://msdn.microsoft.com/library/e9291149-964e-c6fb-4c62-bf2f35a6a0a7%28Office.15%29.aspx) <br/> |[Documents.AfterDocumentMerge Event (Visio)](https://msdn.microsoft.com/library/cac0544d-77b9-b722-cfdb-e42475ce2558%28Office.15%29.aspx) <br/> |
||[Documents.AfterReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/e01c069e-440b-7b8b-8d7d-cdb664f6e2d6%28Office.15%29.aspx) <br/> |
||[Documents.BeforeReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/55a66c47-a2ca-5c8a-2693-aaa1b079c704%28Office.15%29.aspx) <br/> |
||[Documents.QueryCancelReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/d613730e-04c8-d17f-0ad1-19e976aa107d%28Office.15%29.aspx) <br/> |
||[Documents.ReplaceShapesCanceled Event (Visio)](https://msdn.microsoft.com/library/94a20fe7-da09-4e3c-d048-05ba0b8f1070%28Office.15%29.aspx) <br/> |
|[InvisibleApp-Objekt (Visio)](https://msdn.microsoft.com/library/70a30571-2017-af8b-eaa1-bf93c758a46a%28Office.15%29.aspx) <br/> |[InvisibleApp.AfterReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/5d7b8ec2-ef65-1a49-fb50-3fae95d56761%28Office.15%29.aspx) <br/> |
||[InvisibleApp.BeforeReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/bd0e37ca-887a-4d53-3b0c-3339492df3dd%28Office.15%29.aspx) <br/> |
||[InvisibleApp.QueryCancelReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/5e5d9b76-dfd4-1d02-d205-9e64350449d5%28Office.15%29.aspx) <br/> |
||[InvisibleApp.ReplaceShapesCanceled Event (Visio)](https://msdn.microsoft.com/library/17e43497-c7a8-8546-595c-4630afb301a3%28Office.15%29.aspx) <br/> |
|[Page-Objekt (Visio)](https://msdn.microsoft.com/library/7a7f37ab-b448-eb70-b4f1-c185dfbd511e%28Office.15%29.aspx) <br/> |[Page.AfterReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/e4005987-acb1-78d7-91fb-c3c2d5b036e3%28Office.15%29.aspx) <br/> |
||[Page.BeforeReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/57ea9836-74dd-77c2-6541-f8f61b89c0b6%28Office.15%29.aspx) <br/> |
||[Page.Comments Property (Visio)](https://msdn.microsoft.com/library/9618c86c-96c0-be95-ee20-5d1b99f4d5e8%28Office.15%29.aspx) <br/> |
||[Page.Duplicate-Methode (Visio)](https://msdn.microsoft.com/library/394be23b-997d-0da1-b3bd-8278564fb4e0%28Office.15%29.aspx) <br/> |
||[Page.GetTheme Method (Visio)](https://msdn.microsoft.com/library/31c84e69-0bc8-2d1a-84d8-7397110d74ae%28Office.15%29.aspx) <br/> |
||[Page.GetThemeVariant Method (Visio)](https://msdn.microsoft.com/library/40c2be31-fdb0-68ee-a129-2788b1b17c82%28Office.15%29.aspx) <br/> |
||[Page.QueryCancelReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/17ead23f-825a-c608-3315-e2eed6784cd5%28Office.15%29.aspx) <br/> |
||[Page.ReplaceShapesCanceled Event (Visio)](https://msdn.microsoft.com/library/867b1fc1-96bd-cbeb-fd61-b02a96e039ca%28Office.15%29.aspx) <br/> |
||[Page.SetTheme Method (Visio)](https://msdn.microsoft.com/library/5a186f58-9a7a-bd8a-826b-85da75a4d59f%28Office.15%29.aspx) <br/> |
||[Page.SetThemeVariant Method (Visio)](https://msdn.microsoft.com/library/8393a95f-83ca-0efa-d987-ae498bfe5e9d%28Office.15%29.aspx) <br/> |
||[Page.ShapeComments Property (Visio)](https://msdn.microsoft.com/library/b7d86594-ba1f-627b-222f-905da1b1201e%28Office.15%29.aspx) <br/> |
|[Pages-Objekt (Visio)](https://msdn.microsoft.com/library/45eec568-b5cc-5e80-ff5c-4dfa567efb5d%28Office.15%29.aspx) <br/> |[Pages.AfterReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/05c33bdd-e697-d36e-46a8-45705e9ad2c2%28Office.15%29.aspx) <br/> |
||[Pages.BeforeReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/3f6dbc31-0583-dd67-0432-335d6df7a50c%28Office.15%29.aspx) <br/> |
||[Pages.QueryCancelReplaceShapes Event (Visio)](https://msdn.microsoft.com/library/d11ff976-0016-da6b-92fb-379baa7e8f94%28Office.15%29.aspx) <br/> |
||[Pages.ReplaceShapesCanceled Event (Visio)](https://msdn.microsoft.com/library/f0ce8c66-7a15-5f91-8c89-e177bc6671d2%28Office.15%29.aspx) <br/> |
|[Selection-Objekt (Visio)](https://msdn.microsoft.com/library/e5734140-6dbe-7de8-9695-1a22fb4ac628%28Office.15%29.aspx) <br/> |[Selection.ReplaceShape Method (Visio)](https://msdn.microsoft.com/library/dc278901-77ce-e1fe-c44f-f464bbb1c360%28Office.15%29.aspx) <br/> |
||[Selection.SetQuickStyle Method (Visio)](https://msdn.microsoft.com/library/39b810b5-0738-daed-0103-8a2df07559c6%28Office.15%29.aspx) <br/> |
|[Shape-Objekt (Visio)](https://msdn.microsoft.com/library/da7a8872-4ebb-a607-e0ed-eebf68ff5630%28Office.15%29.aspx) <br/> |[Shape.ChangePicture Method (Visio)](https://msdn.microsoft.com/library/9193d802-cebd-2bfd-5f8e-400fac36c1a5%28Office.15%29.aspx) <br/> |
||[Shape.Comments Property (Visio)](https://msdn.microsoft.com/library/498eca91-beb9-b764-0262-a935e5205710%28Office.15%29.aspx) <br/> |
||[Shape.ReplaceShape Method (Visio)](https://msdn.microsoft.com/library/b330a63d-4e3f-0c4d-c38c-6ee806670225%28Office.15%29.aspx) <br/> |
||[Shape.SetQuickStyle Method (Visio)](https://msdn.microsoft.com/library/aebe80cb-fae9-0be7-e903-882f6eb58b63%28Office.15%29.aspx) <br/> |
   
### <a name="new-objects-and-enumerations"></a>Neue Objekte und Aufzählungen

Die folgenden Objekte wurden dem objektmodell Visio hinzugefügt.
  
 **Tabelle 2. Hinzufügungen zum Visio-Objektmodell**
  
|**Objekt**|**Eigenschaften**|**Methoden**|
|:-----|:-----|:-----|
|[CoauthMergeEvent-Objekt (Visio)](https://msdn.microsoft.com/library/eb9425cb-0108-4909-e334-9cd51e5b9303%28Office.15%29.aspx) <br/> |[CoauthMergeEvent.BaseDocument Property (Visio)](https://msdn.microsoft.com/library/7ec09a85-6f51-685b-0c87-4b9eb3266773%28Office.15%29.aspx) <br/> [CoauthMergeEvent.DownloadDocument Property (Visio)](https://msdn.microsoft.com/library/19239540-cd5a-13ea-3b26-282ac3676abd%28Office.15%29.aspx) <br/> [CoauthMergeEvent.ObjectType Property (Visio)](https://msdn.microsoft.com/library/01baa0c2-75b7-2713-9732-1e7a8a7b33aa%28Office.15%29.aspx) <br/> [CoauthMergeEvent.Stat Property (Visio)](https://msdn.microsoft.com/library/d8a96b8e-36b5-c61f-8cea-76266f7eed39%28Office.15%29.aspx) <br/> [CoauthMergeEvent.WorkingDocument Property (Visio)](https://msdn.microsoft.com/library/0f3c4358-0d63-df7f-12fe-7f378bacca86%28Office.15%29.aspx) <br/> |Keine  <br/> |
|[Comment-Objekt (Visio)](https://msdn.microsoft.com/library/f028cc03-0ef1-8017-a936-d30d45211864%28Office.15%29.aspx) <br/> |[Comment.AssociatedObject Property (Visio)](https://msdn.microsoft.com/library/e28eed2e-260e-59c9-9b24-631817fe1ae1%28Office.15%29.aspx) <br/> [Comment.AuthorInitials Property (Visio)](https://msdn.microsoft.com/library/abc07100-8c5c-9982-674d-40b58c096816%28Office.15%29.aspx) <br/> [Comment.AuthorName Property (Visio)](https://msdn.microsoft.com/library/e1da4db8-7a16-16bf-2a5f-be1ac5372d34%28Office.15%29.aspx) <br/> [Comment.AuthorSipAddress Property (Visio)](https://msdn.microsoft.com/library/f8d185a9-91b6-471a-3c0e-ffa8a06b36b3%28Office.15%29.aspx) <br/> [Comment.AuthorSMTPAddress Property (Visio)](https://msdn.microsoft.com/library/22e04ccc-c524-ca08-d5e2-db68fdb3afb6%28Office.15%29.aspx) <br/> [Comment.Collapsed Property (Visio)](https://msdn.microsoft.com/library/9552e379-e351-78d7-e0ed-4f524c3273a1%28Office.15%29.aspx) <br/> [Comment.CreateDate Property (Visio)](https://msdn.microsoft.com/library/b643e13e-da12-a992-3a59-99b37f003fb9%28Office.15%29.aspx) <br/> [Comment.Document Property (Visio)](https://msdn.microsoft.com/library/d57b1377-b895-1fe1-2f98-ef000fdd9c39%28Office.15%29.aspx) <br/> [Comment.EditDate Property (Visio)](https://msdn.microsoft.com/library/4ad13f54-215e-3680-5de6-13715e309fbf%28Office.15%29.aspx) <br/> [Comment.ObjectType Property (Visio)](https://msdn.microsoft.com/library/bf0d786d-e1b6-65f1-3112-5dfd4ff324e9%28Office.15%29.aspx) <br/> [Comment.Stat Property (Visio)](https://msdn.microsoft.com/library/f457598c-af42-cb83-ecd2-4fd42898ea16%28Office.15%29.aspx) <br/> [Comment.Text Property (Visio)](https://msdn.microsoft.com/library/3ec63034-de5f-d9f2-16a5-e06a56883867%28Office.15%29.aspx) <br/> |[Comment.Delete Method (Visio)](https://msdn.microsoft.com/library/7762f264-f680-5758-7c35-dfe9067b61ca%28Office.15%29.aspx) <br/> |
|[Comments-Objekt (Visio)](https://msdn.microsoft.com/library/7cd0ee53-6b8d-a03b-ecd6-f6f6dda0f2d4%28Office.15%29.aspx) <br/> |[Comments.Count Property (Visio)](https://msdn.microsoft.com/library/abac02d5-5047-2c9d-5c5c-e2738f99a4a6%28Office.15%29.aspx) <br/> [Comments.Document Property (Visio)](https://msdn.microsoft.com/library/507d4698-e282-f8a9-1299-c67945ee5fc4%28Office.15%29.aspx) <br/> [Comments.Item Property (Visio)](https://msdn.microsoft.com/library/fed2a079-de87-d5ce-1d74-0bfa5a328441%28Office.15%29.aspx) <br/> [Comments.ObjectType Property (Visio)](https://msdn.microsoft.com/library/06544d73-ce00-2c89-1ecb-20541b251d57%28Office.15%29.aspx) <br/> [Comments.Stat Property (Visio)](https://msdn.microsoft.com/library/1f5f29b2-236c-91b6-6d25-7bacc37ca96c%28Office.15%29.aspx) <br/> |[Comments.Add Method (Visio)](https://msdn.microsoft.com/library/da02de49-8057-7e5c-6b59-0a013e56256d%28Office.15%29.aspx) <br/> [Comments.DeleteAll Method (Visio)](https://msdn.microsoft.com/library/50777ed3-553c-90ae-2d30-9dde412fe6b9%28Office.15%29.aspx) <br/> |
|[ReplaceShapesEvent-Objekt (Visio)](https://msdn.microsoft.com/library/26c4e7cb-6618-6d2f-a4be-515584f8cd10%28Office.15%29.aspx) <br/> |[ReplaceShapesEvent.ObjectType Property (Visio)](https://msdn.microsoft.com/library/bcc442f0-aa4e-cd5a-d116-f3fb74459927%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.ReplaceFlags Property (Visio)](https://msdn.microsoft.com/library/d0d00891-c794-bd0c-d37e-1ab98c92beab%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.ReplacementMaster Property (Visio)](https://msdn.microsoft.com/library/326a1889-8952-b4ac-c5c0-ac4470257c06%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.SelectionSource Property (Visio)](https://msdn.microsoft.com/library/f81c0b66-b63b-fc7c-1769-d56a17d5cf78%28Office.15%29.aspx) <br/> [ReplaceShapesEvent.Stat Property (Visio)](https://msdn.microsoft.com/library/96f3d382-5dda-7f93-088d-96edc831cd7c%28Office.15%29.aspx) <br/> |Keine  <br/> |
   
In der folgenden Tabelle sind die neuen Enumerationen und Konstanten aufgeführt, die in Visio 2013 eingeführt wurden.
  
 **Tabelle 3. Hinzugefügte Visio-Aufzählungen**
  
|**Enumeration**|**Beschreibung**|
|:-----|:-----|
|[VisQuickStyleColors Enumeration (Visio)](https://msdn.microsoft.com/library/c19d91f3-a9a4-e31e-ed7a-eef15553fbf4%28Office.15%29.aspx) <br/> |Gibt festgelegte Namen für Farben innerhalb eines Designs an  <br/> |
|[VisQuickStyleMatrixIndices Enumeration (Visio)](https://msdn.microsoft.com/library/0fb0b448-85ba-4fc4-d933-21d574cefa2a%28Office.15%29.aspx) <br/> |Gibt festgelegte Namen für die Designs und Variationen an, die mit Visio 2013 bereitgestellt werden.  <br/> |
|[VisReplaceFlags Enumeration (Visio)](https://msdn.microsoft.com/library/cf270178-f939-7eb4-b8e1-3b4153aff221%28Office.15%29.aspx) <br/> |Gibt Verhaltensweisen für den Vorgang "Shape ändern" an  <br/> |
|[VisSVGExportFormat Enumeration (Visio)](https://msdn.microsoft.com/library/d8ca8c3f-41d9-4e9d-8f6d-f5567361b14e%28Office.15%29.aspx) <br/> |Gibt den Einschluss oder Ausschluss von Visio-Markup beim Exportieren eines Diagramms nach SVG an  <br/> |
   
### <a name="deprecated-objects-and-members"></a>Veraltete Objekte und Member

In der folgenden Tabelle sind die veralteten Objekte und Member aufgeführt, die in Visio 2013 eingeführt wurden. In der Spalte **Veraltete Member** werden nur veraltete Objektmember aufgeführt. 
  
 **Tabelle 4. Veraltete Elemente im Visio-Objektmodell**
  
|**Objekt oder Auflistung**|**Veraltete Member**|
|:-----|:-----|
|**Window-Objekt**  <br/> |**PageTabWidth**-Eigenschaft  <br/> |
   
## <a name="see-also"></a>Siehe auch
<a name="vis15_WhatsNew_Additional"> </a>

- [Visio für Entwickler](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [Neuigkeiten für Visio ShapeSheet-Entwickler](what-s-new-for-visio-shapesheet-developers.md)
    
- [Visio Services in SharePoint 2013](https://msdn.microsoft.com/library/jj164027%28office.15%29.aspx)
    
- [Neues in Visio (Office.com)](https://office.com/redir/HA102749364.aspx)
    
- [Visio Developer Center](https://msdn.microsoft.com/office/aa905478.aspx)
    

