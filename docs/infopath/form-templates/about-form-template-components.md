---
title: Informationen zu Formularvorlagenkomponenten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b51361fe-cf29-f890-9876-5aebe15c73e1
description: Microsoft InfoPath-Formularvorlagen bestehen mehrere Dateien und Komponenten, die kombiniert werden, um bestimmte Funktionen für einen bestimmten Benutzer End Szenario oder Business Notwendigkeit bereitzustellen. InfoPath-Formularen variiert je nach den Typ des erforderlich komplexer, dass Sie sich beziehen.
ms.openlocfilehash: 4ef90d3fb55ee38018d2c1226bef5fd59e277186
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790718"
---
# <a name="about-form-template-components"></a>Informationen zu Formularvorlagenkomponenten

Microsoft InfoPath-Formularvorlagen bestehen mehrere Dateien und Komponenten, die kombiniert werden, um bestimmte Funktionen für einen bestimmten Benutzer End Szenario oder Business Notwendigkeit bereitzustellen. InfoPath-Formularen variiert je nach den Typ des erforderlich komplexer, dass Sie sich beziehen.
  
Bei einer InfoPath-Formularvorlage handelt es sich im Prinzip um einen Anwendungstyp, mit dem eine angegebene Klasse von XML-Dokumenten erstellt wird, deren Layout und Bearbeitungsverhalten definiert wird, deren Datenkonsistenz erzwungen wird sowie die Routinginformationen für den Speicherort der Dokumente bereitgestellt werden.
  
Sie sollten unbedingt beachten, dass InfoPath-Formularvorlagen aus mehreren Dateien unterschiedlichen Typs bestehen. Diese Dateien zusammen werden als Formulardateien bezeichnet. In der Regel besteht eine InfoPath-Formularvorlage aus den folgenden Dateitypen.
  
|**Name**|**Erweiterung**|**Beschreibung**|
|:-----|:-----|:-----|
|Formulardefinition  <br/> |XSF  <br/> |Eine von InfoPath generierte Datei, die Informationen zu allen anderen in einem Formular verwendeten Dateien und Komponenten enthält. Diese Datei dient als Manifest für das Formular.  <br/> |
|XML-Schema  <br/> |XSD  <br/> |Die XML-Schemadateien, mit denen die zugrunde liegenden Dokumentdateien eines Formulars eingeschränkt und überprüft werden.  <br/> |
|Ansicht  <br/> |XSL  <br/> |Die Präsentationslogikdateien, mit denen die in den zugrunde liegenden XML-Dokumentdateien eines Formulars enthaltenen Daten präsentiert, angezeigt und transformiert werden.  <br/> |
|XML-Vorlage   <br/> |XML  <br/> |Die XML-Datei mit den Standarddaten, die in einer Ansicht beim Erstellen eines neuen Formulars angezeigt werden.  <br/> |
|Präsentation  <br/> |HTM, GIF, BMP usw.  <br/> |Die Dateien, die zusammen mit den Ansichtsdateien zum Erstellen einer benutzerdefinierten Benutzeroberfläche verwendet werden.  <br/> |
|Geschäftslogik  <br/> |DLL  <br/> |Der kompilierte Programmiercode, mit dem ein bestimmtes Bearbeitungsverhalten, die Datenüberprüfung, Ereignishandler, die Kontrolle des Datenflusses und weitere benutzerdefinierte Geschäftslogik implementiert werden. InfoPath-Geschäftslogik kann in den Programmiersprachen Visual Basic und C# .NET geschrieben werden, die als Binärdateien kompiliert und eingeschlossen werden.  <br/> |
|Binärdateien  <br/> |DLL, EXE  <br/> |  Alle benutzerdefinierten Komponenten, die zusätzliche Geschäftslogik bereitstellen.  <br/> |
|Formularvorlage  <br/> |XSN  <br/> |Das komprimierte Dateiformat (CAB), mit dem alle Formulardateien zu einer einzigen Datei zusammengefasst werden.  <br/> |
   

