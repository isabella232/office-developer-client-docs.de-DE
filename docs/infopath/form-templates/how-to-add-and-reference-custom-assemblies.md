---
title: Hinzufügen und Verweisen auf benutzerdefinierte Assemblys
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen mithilfe von benutzerdefinierten Assemblys,Assemblys [InfoPath 2007], Hinzufügen von benutzerdefinierten Formularvorlagen mithilfe des InfoPath 2003-Objektmodells
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Wenn Sie in einem Formularvorlagenprojekt mit verwaltetem Code einen Verweis auf eine benutzerdefinierte Assembly hinzufügen, wird diese beim Kompilieren und Veröffentlichen des Projekts in die Formularvorlagendatei (XSN) einbezogen.
ms.openlocfilehash: 19b5f06231bb03cfac8b32b157e03956b5fc334e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431169"
---
# <a name="add-and-reference-custom-assemblies"></a>Hinzufügen und Verweisen auf benutzerdefinierte Assemblys

Wenn Sie in einem Formularvorlagenprojekt mit verwaltetem Code einen Verweis auf eine benutzerdefinierte Assembly hinzufügen, wird diese beim Kompilieren und Veröffentlichen des Projekts in die Formularvorlagendatei (XSN) einbezogen.
  
## <a name="add-and-reference-a-custom-assembly"></a>Hinzufügen einer benutzerdefinierten Assembly und Verweisen darauf

Zur Vermeidung eines Konflikts mit der Art und Weise, wie vom InfoPath-Projektsystem Dateien verwaltet werden, die der Formularvorlagendatei hinzugefügt werden, kopieren Sie keine benutzerdefinierten Assemblys, auf die Sie verweisen möchten, in den Ordner auf der obersten Ebene eines Formularvorlagenprojekts. Standardmäßig ist dies ein Pfad im folgenden Format: < *Laufwerk*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName* 
  
Wenn Sie benutzerdefinierte Assemblys verschieben möchten, die Sie auf einen Speicherort im Projektordner verweisen, müssen Sie einen Unterordner unter dem Projekthauptordner erstellen und anschließend die benutzerdefinierten Assemblys aus dem Unterordnerkopieren und darauf verweisen. Beachten Sie jedoch, dass das Erstellen eines Unterordners für Assemblys, auf die verwiesen wird, nicht erforderlich ist. Sofern sich eine Assembly, auf die verwiesen wird, nicht im Ordner auf der höchsten Ebene des Projekts befindet, wird sie vom InfoPath-Projektsystem beim Kompilieren und Veröffentlichen des Projekts automatisch in die Formularvorlagendatei (XSN) kopiert.
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>Verweisen auf eine benutzerdefinierte Assembly von ihrem Standardspeicherort aus

1. Öffnen Sie das Formularvorlagenprojekt in Visual Studio 2012.
    
2. Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.
    
3. Klicken Sie auf die Registerkarte **Durchsuchen**, bestimmen Sie die Assembly, und klicken Sie dann auf **OK**, um den Verweis hinzuzufügen. 
    
## <a name="see-also"></a>Siehe auch

#### <a name="tasks"></a>Aufgaben

[Erstellen einer Formularvorlage mithilfe des InfoPath 2003-Objektmodells](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

