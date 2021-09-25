---
title: Verwenden SharePoint-Objektmodellmember
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Bevor Sie mit Elementen des SharePoint-Objektmodells aus Code programmieren können, der in einer InfoPath-Formularvorlage ausgeführt wird, müssen Sie auf die Microsoft.SharePoint.dll Assembly im Projekt Visual Studio 2012 für Ihr Formular verweisen. Dazu müssen Sie Zugriff auf das Dateisystem einer lizenzierten Kopie von Microsoft SharePoint Server 2010 oder eines Servers haben, auf dem Microsoft SharePoint Foundation 2010 ausgeführt wird, damit Sie eine Kopie der Microsoft.SharePoint.dll Assembly abrufen können.
ms.openlocfilehash: 487900d890edb0aaa8549f2c875a0ec4dd554781
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584829"
---
# <a name="use-sharepoint-object-model-members"></a>Verwenden SharePoint-Objektmodellmember

Bevor Sie mit Elementen des SharePoint-Objektmodells aus Code programmieren können, der in einer InfoPath-Formularvorlage ausgeführt wird, müssen Sie auf die Microsoft.SharePoint.dll Assembly im Projekt Visual Studio 2012 für Ihr Formular verweisen. Dazu müssen Sie Zugriff auf das Dateisystem einer lizenzierten Kopie von Microsoft SharePoint Server 2010 oder eines Servers haben, auf dem Microsoft SharePoint Foundation 2010 ausgeführt wird, damit Sie eine Kopie der Microsoft.SharePoint.dll Assembly abrufen können. 
  
Darüber hinaus muss Ihre Formularvorlage auf dem Server als Sandkasten- oder vom Administrator genehmigte Lösung bereitgestellt werden. Weitere Informationen zu diesen Bereitstellungsoptionen finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Hinzufügen von und Verweisen auf die Microsoft.SharePoint-Assembly in einer InfoPath-Formularvorlage

> [!IMPORTANT]
> Um einen Konflikt bei der Verwaltung von Dateien durch das InfoPath-Projektsystem zu vermeiden, die der Formularvorlagendatei hinzugefügt werden, kopieren Sie keine Assemblys, auf die Sie im Ordner auf höchster Ebene des Formularvorlagenprojekts verweisen möchten. Standardmäßig ist dies ein Pfad im folgenden Format: < *Laufwerk*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName* > Wenn Sie Assemblys verschieben möchten, auf die Sie im Projektordner verweisen, müssen Sie einen Unterordner unter dem  *ProjectName-Hauptprojektordner*  erstellen und dann Assemblys aus diesem Unterordner kopieren und darauf verweisen. Beachten Sie jedoch, dass das Erstellen eines Unterordners für Assemblys, auf die verwiesen wird, nicht erforderlich ist. Sofern sich eine Assembly, auf die verwiesen wird, nicht im Ordner auf der höchsten Ebene des Projekts befindet, wird sie vom InfoPath-Projektsystem beim Kompilieren und Veröffentlichen des Projekts automatisch in die Formularvorlagendatei (XSN) kopiert. 
  
Standardmäßig wird Microsoft.SharePoint.Server.dll in C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI im Dateisystem von SharePoint Server 2010 oder auf einem Server installiert, auf dem SharePoint Foundation 2010 ausgeführt wird.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>So verweisen Sie im Codeprojekt eines InfoPath-Formulars auf die Microsoft.SharePoint-Assembly

1. Kopieren Sie die Microsoft.SharePoint.Server.dll-Assembly vom Server in einen lokalen Ordner, oder greifen Sie über einen freigegebenen Ordner auf die Assembly zu.
    
2. Öffnen Sie das Formularvorlagenprojekt in Visual Studio 2012.
    
3. Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.
    
4. Klicken Sie auf die Registerkarte **Durchsuchen**, bestimmen Sie die Assembly, und klicken Sie dann auf **OK**, um den Verweis hinzuzufügen. 
    
Jetzt können Sie Code für Elemente des SharePoint-Objektmodells aus dem Formularcode schreiben. Um es einfacher zu machen, auf Mitglieder von Microsoft zu verweisen. SharePoint Namespace, fügen Sie `using Microsoft.SharePoint;` die Direktiven am Anfang der Codedatei hinzu oder fügen Sie sie `Imports Microsoft.SharePoint` hinzu. Ein Beispiel, das zeigt, wie Elemente des SharePoint-Objektmodells in einem InfoPath-Formular verwendet werden, finden Sie unter "Beispiel 2: Verwalten von Anbietern in einer SharePoint Liste" in [Beispiel-Sandkastenlösungen.](sample-sandboxed-solutions.md)

