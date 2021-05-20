---
title: Verwenden SharePoint Objektmodellm members
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Bevor Sie elemente des SharePoint-Objektmodells aus Code programmieren können, der in einer InfoPath-Formularvorlage ausgeführt wird, müssen Sie im Visual Studio 2012-Projekt für Ihr Formular auf die Microsoft.SharePoint.dll-Assembly verweisen. Dazu müssen Sie zugriff auf das Dateisystem einer lizenzierten Kopie von Microsoft SharePoint Server 2010 oder eines Servers haben, auf dem Microsoft SharePoint Foundation 2010 ausgeführt wird, damit Sie eine Kopie der Microsoft.SharePoint.dll erhalten können.
ms.openlocfilehash: e29725450a6a1bdcba99215e337493f8686491e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431659"
---
# <a name="use-sharepoint-object-model-members"></a>Verwenden SharePoint Objektmodellm members

Bevor Sie elemente des SharePoint-Objektmodells aus Code programmieren können, der in einer InfoPath-Formularvorlage ausgeführt wird, müssen Sie im Visual Studio 2012-Projekt für Ihr Formular auf die Microsoft.SharePoint.dll-Assembly verweisen. Dazu müssen Sie zugriff auf das Dateisystem einer lizenzierten Kopie von Microsoft SharePoint Server 2010 oder eines Servers haben, auf dem Microsoft SharePoint Foundation 2010 ausgeführt wird, damit Sie eine Kopie der Microsoft.SharePoint.dll erhalten können. 
  
Darüber hinaus muss Ihre Formularvorlage auf dem Server als Sandkasten- oder vom Administrator genehmigte Lösung bereitgestellt werden. Weitere Informationen zu diesen Bereitstellungsoptionen finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Hinzufügen von und Verweisen auf die Microsoft.SharePoint-Assembly in einer InfoPath-Formularvorlage

> [!IMPORTANT]
> Um einen Konflikt bei der Verwaltung von Dateien durch das InfoPath-Projektsystem zu vermeiden, die der Formularvorlagendatei hinzugefügt werden, kopieren Sie keine Assemblys, auf die Sie im Ordner auf höchster Ebene des Formularvorlagenprojekts verweisen möchten. Standardmäßig ist dies ein Pfad im folgenden Format: *<*  laufwerk >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName* > Wenn Sie Assemblys verschieben möchten, auf die Sie im Projektordner verweisen, müssen Sie einen Unterordner unter dem Projektordner  *ProjectName*  erstellen und dann Assemblys aus diesem Unterordner kopieren und darauf verweisen. Beachten Sie jedoch, dass das Erstellen eines Unterordners für Assemblys, auf die verwiesen wird, nicht erforderlich ist. Sofern sich eine Assembly, auf die verwiesen wird, nicht im Ordner auf der höchsten Ebene des Projekts befindet, wird sie vom InfoPath-Projektsystem beim Kompilieren und Veröffentlichen des Projekts automatisch in die Formularvorlagendatei (XSN) kopiert. 
  
Standardmäßig ist Microsoft.SharePoint.Server.dll im Dateisystem von SharePoint Server 2010 oder auf einem Server mit SharePoint Foundation 2010 in C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI installiert.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>So verweisen Sie im Codeprojekt eines InfoPath-Formulars auf die Microsoft.SharePoint-Assembly

1. Kopieren Sie die Microsoft.SharePoint.Server.dll-Assembly vom Server in einen lokalen Ordner, oder greifen Sie über einen freigegebenen Ordner auf die Assembly zu.
    
2. Öffnen Sie das Formularvorlagenprojekt in Visual Studio 2012.
    
3. Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.
    
4. Klicken Sie auf die Registerkarte **Durchsuchen**, bestimmen Sie die Assembly, und klicken Sie dann auf **OK**, um den Verweis hinzuzufügen. 
    
Jetzt können Sie Code für Elemente des SharePoint Aus dem Formularcode schreiben. Um den Verweis auf Mitglieder von Microsoft zu erleichtern. SharePoint Namespace hinzufügen oder den Direktiven am Anfang `using Microsoft.SharePoint;` `Imports Microsoft.SharePoint` der Codedatei hinzufügen. Ein Beispiel für die Verwendung von Mitgliedern des SharePoint-Objektmodells in einem InfoPath-Formular finden Sie unter "Beispiel 2: Verwalten von Anbietern in einer SharePoint-Liste" unter [Beispiel](sample-sandboxed-solutions.md)sandkastenlösungen .

