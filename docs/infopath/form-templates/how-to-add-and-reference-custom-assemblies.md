---
title: Hinzufügen von und verweisen auf benutzerdefinierte Assemblys
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen verwenden benutzerdefinierter Assemblys, Assemblys [InfoPath 2007], Hinzufügen benutzerdefinierter mithilfe des InfoPath 2003-Objektmodell
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Wenn Sie in einem Formularvorlagenprojekt mit verwaltetem Code einen Verweis auf eine benutzerdefinierte Assembly hinzufügen, wird diese beim Kompilieren und Veröffentlichen des Projekts in die Formularvorlagendatei (XSN) einbezogen.
ms.openlocfilehash: e182930ebe14b6f64d1b90509fe400cc1fb1b26e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790730"
---
# <a name="add-and-reference-custom-assemblies"></a>Hinzufügen von und verweisen auf benutzerdefinierte Assemblys

Wenn Sie in einem Formularvorlagenprojekt mit verwaltetem Code einen Verweis auf eine benutzerdefinierte Assembly hinzufügen, wird diese beim Kompilieren und Veröffentlichen des Projekts in die Formularvorlagendatei (XSN) einbezogen.
  
## <a name="add-and-reference-a-custom-assembly"></a>Hinzufügen einer benutzerdefinierten Assembly und Verweisen darauf

Kopieren Sie zum Vermeiden von eines Konflikts mit wie das InfoPath-Projektsystem Dateien verwaltet wird, die die Formularvorlagendatei hinzugefügt werden, keine benutzerdefinierte Assemblys, die Sie in den Ordner der obersten Ebene des ein Formularvorlagenprojekt verweisen möchten. Standardmäßig wird dies einen Pfad in folgendem Format sein: < *Laufwerk* >: \Users\ *UserName* \Documents\InfoPath Projects\ *Projektname* 
  
Wenn Sie benutzerdefinierte Assemblys verschieben möchten, die Sie auf einen Speicherort im Projektordner verweisen, müssen Sie einen Unterordner unter dem Projekthauptordner erstellen und anschließend die benutzerdefinierten Assemblys aus dem Unterordnerkopieren und darauf verweisen. Beachten Sie jedoch, dass das Erstellen eines Unterordners für Assemblys, auf die verwiesen wird, nicht erforderlich ist. Sofern sich eine Assembly, auf die verwiesen wird, nicht im Ordner auf der höchsten Ebene des Projekts befindet, wird sie vom InfoPath-Projektsystem beim Kompilieren und Veröffentlichen des Projekts automatisch in die Formularvorlagendatei (XSN) kopiert.
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>Verweisen auf eine benutzerdefinierte Assembly von ihrem Standardspeicherort aus

1. Öffnen Sie das Formularvorlagenprojekt in Visual Studio 2012.
    
2. On the **Project** menu, click **Add Reference**.
    
3. Klicken Sie auf die Registerkarte **Durchsuchen** , suchen Sie und geben Sie die Assembly, und klicken Sie dann auf **OK** , um den Verweis hinzuzufügen. 
    
## <a name="see-also"></a>Siehe auch

#### <a name="tasks"></a>Aufgaben

[Erstellen einer Formularvorlage mit dem InfoPath 2003-Objektmodell](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

