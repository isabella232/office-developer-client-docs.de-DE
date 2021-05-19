---
title: Informationen zu Formularvorlagenkomponenten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b51361fe-cf29-f890-9876-5aebe15c73e1
description: Microsoft InfoPath-Formularvorlagen bestehen aus mehreren Dateien und Komponenten, die kombiniert werden, um bestimmte Funktionen für ein bestimmtes Endbenutzerszenario oder geschäftsspezifische Anforderungen bereitzustellen. Die Komplexität von InfoPath-Formularen hängt von den jeweiligen Anforderungen ab.
ms.openlocfilehash: 3c5adc7ec1e24af481dff7f4a8d009b2dcb6ba8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419058"
---
# <a name="about-form-template-components"></a>Informationen zu Formularvorlagenkomponenten

Microsoft InfoPath-Formularvorlagen bestehen aus mehreren Dateien und Komponenten, die kombiniert werden, um bestimmte Funktionen für ein bestimmtes Endbenutzerszenario oder geschäftsspezifische Anforderungen bereitzustellen. Die Komplexität von InfoPath-Formularen hängt von den jeweiligen Anforderungen ab.
  
Bei einer InfoPath-Formularvorlage handelt es sich im Prinzip um einen Anwendungstyp, mit dem eine angegebene Klasse von XML-Dokumenten erstellt wird, deren Layout und Bearbeitungsverhalten definiert wird, deren Datenkonsistenz erzwungen wird sowie die Routinginformationen für den Speicherort der Dokumente bereitgestellt werden.
  
Sie sollten unbedingt beachten, dass InfoPath-Formularvorlagen aus mehreren Dateien unterschiedlichen Typs bestehen. Diese Dateien zusammen werden als Formulardateien bezeichnet. In der Regel besteht eine InfoPath-Formularvorlage aus den folgenden Dateitypen.
  
|**Name**|**Erweiterung**|**Beschreibung**|
|:-----|:-----|:-----|
|Formulardefinition  <br/> |XSF  <br/> |Eine von InfoPath generierte Datei, die Informationen zu allen anderen in einem Formular verwendeten Dateien und Komponenten enthält. Diese Datei dient als Manifest für das Formular.  <br/> |
|XML-Schema  <br/> |.xsd  <br/> |Die XML-Schemadateien, mit denen die zugrunde liegenden Dokumentdateien eines Formulars eingeschränkt und überprüft werden.  <br/> |
|Anzeigen  <br/> |.xsl  <br/> |Die Präsentationslogikdateien, mit denen die in den zugrunde liegenden XML-Dokumentdateien eines Formulars enthaltenen Daten präsentiert, angezeigt und transformiert werden.  <br/> |
|XML-Vorlage  <br/> |.xml  <br/> |Die XML-Datei mit den Standarddaten, die in einer Ansicht beim Erstellen eines neuen Formulars angezeigt werden.  <br/> |
|Präsentation  <br/> |HTM, GIF, BMP usw.  <br/> |Die Dateien, die zusammen mit den Ansichtsdateien zum Erstellen einer benutzerdefinierten Benutzeroberfläche verwendet werden.  <br/> |
|Geschäftslogik  <br/> |.dll  <br/> |Der kompilierte Programmiercode, mit dem ein bestimmtes Bearbeitungsverhalten, die Datenüberprüfung, Ereignishandler, die Kontrolle des Datenflusses und weitere benutzerdefinierte Geschäftslogik implementiert werden. InfoPath-Geschäftslogik kann in den Programmiersprachen Visual Basic und C# .NET geschrieben werden, die als Binärdateien kompiliert und eingeschlossen werden.  <br/> |
|Binär  <br/> |.dll, .exe  <br/> | Alle benutzerdefinierten Komponenten, die zusätzliche Geschäftslogik bereitstellen.  <br/> |
|Formularvorlage  <br/> |XSN  <br/> |Das komprimierte Dateiformat (CAB), mit dem alle Formulardateien zu einer einzigen Datei zusammengefasst werden.  <br/> |
   

