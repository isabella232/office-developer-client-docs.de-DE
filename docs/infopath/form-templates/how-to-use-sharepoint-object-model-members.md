---
title: Verwenden von SharePoint-Objektmodellmember
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Bevor Sie Mitglied der SharePoint-Objektmodell aus in eine InfoPath-Formularvorlage ausgeführten Code programmieren können, müssen Sie für Ihr Formular die Microsoft.SharePoint.dll-Assembly in Visual Studio 2012-Projekt referenzieren. Klicken Sie dazu benötigen Sie Zugriff auf das Dateisystem der eine lizenzierte Version von Microsoft SharePoint Server 2010 oder einen Server, auf der Microsoft SharePoint Foundation 2010 ausgeführt wird, damit Sie eine Kopie der Microsoft.SharePoint.dll-Assembly abrufen können.
ms.openlocfilehash: c496f603f50a55ae2eaee237d6910d92612e1761
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790741"
---
# <a name="use-sharepoint-object-model-members"></a>Verwenden von SharePoint-Objektmodellmember

Bevor Sie Mitglied der SharePoint-Objektmodell aus in eine InfoPath-Formularvorlage ausgeführten Code programmieren können, müssen Sie für Ihr Formular die Microsoft.SharePoint.dll-Assembly in Visual Studio 2012-Projekt referenzieren. Klicken Sie dazu benötigen Sie Zugriff auf das Dateisystem der eine lizenzierte Version von Microsoft SharePoint Server 2010 oder einen Server, auf der Microsoft SharePoint Foundation 2010 ausgeführt wird, damit Sie eine Kopie der Microsoft.SharePoint.dll-Assembly abrufen können. 
  
Darüber hinaus muss die Formularvorlage auf dem Server als Sandkastenmodus oder vom Administrator genehmigten Lösung bereitgestellt werden. Weitere Informationen zu diesen Bereitstellungsoptionen finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Hinzufügen von und Verweisen auf die Microsoft.SharePoint-Assembly in einer InfoPath-Formularvorlage

> [!IMPORTANT]
> Kopieren Sie zum Vermeiden von eines Konflikts mit wie das InfoPath-Projektsystem Dateien verwaltet wird, die die Formularvorlagendatei hinzugefügt werden, keine Assemblys, die Sie in den Ordner der obersten Ebene des ein Formularvorlagenprojekt verweisen möchten. Standardmäßig wird dies einen Pfad in folgendem Format sein: < *Laufwerk* >: \Users\ *UserName* \Documents\InfoPath Projects\ *Projektname* > Wenn Sie Assemblys, die Sie verweisen auf eine Position im Projektordner, verschieben möchten, Sie muss erstellen Sie einen Unterordner unter dem Hauptfenster *Projektname* Projektordner, und klicken Sie dann kopieren und Verweisassemblys aus diesem Unterordner. Beachten Sie jedoch, dass erstellen einen Unterordner für Verweisassemblys nicht erforderlich ist. Solange eine referenzierte Assembly nicht im Ordner der obersten Ebene des Projekts gefunden wird, wird die InfoPath-Projektsystems kopieren Sie die Assembly in der Formularvorlagendatei (XSN), wenn das Projekt kompiliert und veröffentlicht wird. 
  
Standardmäßig ist die Microsoft.SharePoint.Server.dll in C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI im Dateisystem des SharePoint Server 2010 oder einen Server mit SharePoint Foundation 2010 installiert.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>So verweisen Sie im Codeprojekt eines InfoPath-Formulars auf die Microsoft.SharePoint-Assembly

1. Kopieren Sie die Microsoft.SharePoint.Server.dll-Assembly vom Server in einen lokalen Ordner, oder greifen Sie über einen freigegebenen Ordner auf die Assembly zu.
    
2. Öffnen Sie das Formularvorlagenprojekt in Visual Studio 2012.
    
3. On the **Project** menu, click **Add Reference**.
    
4. Klicken Sie auf die Registerkarte **Durchsuchen** , suchen Sie und geben Sie die Assembly, und klicken Sie dann auf **OK** , um den Verweis hinzuzufügen. 
    
Jetzt können Sie Code für Member des SharePoint-Objektmodells in Ihrem Formularcode schreiben. Hinzufügen, um zum Verweisen auf Elemente des Microsoft.SharePoint-Namespace erleichtern, `using Microsoft.SharePoint;` oder `Imports Microsoft.SharePoint` an die Direktiven am Anfang der Codedatei. Ein Beispiel, das zeigt, wie Sie Mitglieder des SharePoint-Objektmodells in einem InfoPath-Formular zu verwenden, finden Sie unter "Beispiel 2: Verwalten von Anbietern in einer SharePoint-Liste" in [Beispiele für Sandkastenlösungen](sample-sandboxed-solutions.md).

