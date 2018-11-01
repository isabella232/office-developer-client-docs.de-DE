---
title: Verwenden des Java-Typbibliotheks-Assistenten
TOCTitle: Using the Java Type Library Wizard
ms:assetid: 96af770c-c7c2-c905-3c3e-383a5b99cab2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249670(v=office.15)
ms:contentKeyID: 48546455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 233e1a9e6237500b3d13e3234e7c6ddf4d556abc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884135"
---
# <a name="using-the-java-type-library-wizard"></a>Verwenden des Java-Typbibliotheks-Assistenten


**Betrifft**: Access 2013, Office 2013

Der Java-Typbibliotheks-Assistent ist ein Feature von Visual J++ 1.x, das in das Menü **Extras** der Entwicklungsumgebung integriert ist. Er dient zum Durchsuchen einer Typbibliothek und zum Erstellen einer Java-Schnittstelle, die den Zugriff auf COM-Objekte ermöglicht. Für Visual J++ 6.0 wurde der Java-Typbibliotheks-Assistent ersetzt durch [ADO für Windows Foundation Classes](ado-wfc-programming.md).

Die mit dem Java-Typbibliotheks-Assistenten erzeugten Ergebnisse ähneln denen der Befehlszeilentools, die im [Microsoft SDK für Java](using-the-microsoft-sdk-for-java.md) enthalten sind. Sie können jedoch im Gegensatz zu den vom Microsoft SDK für Java generierten Klassenwrappern nicht in die vom Assistenten generierten Klassenwrapper springen.

Der Java-Typbibliotheks-Assistenten generiert die Klassen, die an folgendem Speicherort: \\ \<Windows-Verzeichnis\>\\Java\\Trustlib\\msado15. Die Datei Summary.txt in das Verzeichnis, in dem die Klassen generiert wurden, zeigt die Klassendefinitionen erstellte.

Durch den Java-Typbibliotheks-Assistenten werden Aufzählungstypen aus beliebigen Typbibliotheken in den INT-Typ (Ganzzahl) konvertiert. Außerdem wird eine Schnittstelle definiert, die den einzelnen Aufzählungstypen in der Typbibliothek entspricht. Sie können mit der folgenden Syntax auf die Werte eines ADO-Aufzählungstyps verweisen:

```vb 
 
msado15.<Enum Name>.<constant Name> 
```

Ein Beispiel hierfür wird im folgenden Codefragment für das Festlegen der **CommandType** -Eigenschaft eines **Command** -Objekts gezeigt:

```vb 
 
Cmd1.putCommandType( msado15.CommandTypeEnum.adCmdStoredProc ); 
```

Alternativ konnte die von der Java-Typbibliotheks-Assistenten generierte Aufzählungstyp Wrapper vererben. Wenn dies der Fall ist, können Sie "msado15." entfernen. von der Syntax. Jedoch die Klasse von jedem Java-Objekt erbt müssten und aufgezählt Typschnittstelle, die darauf verweist, um die Notwendigkeit, msado15 verweisen vollständig zu entfernen. \* vor alle ADO-Objekte und Enumerationswerte.

Weiteren Beispielcode finden Sie unter [ADO-Java-Klassenwrapper](ado-java-class-wrappers.md).

**Zum Ausführen der Java-Typbibliotheks-Assistenten aus Visual J++, Version 1.*x***

1.  Wählen Sie im Menü **Extras** die Option **Java-Typbibliotheks-Assistent** aus.

2.  Wählen Sie "Microsoft ActiveX Data Objects Library" aus, und klicken Sie auf **OK**. Diese jetzt (Re) generiert Dateien in die \\Trustlib-Verzeichnis für ADO (standardmäßig unter c:\\Winnt\\Java\\Trustlib\\msado15). Wenn Sie bereits Klassen für ADO Generieren des Microsoft SDK für Java verwendet, werden sie durch die die Java-Typbibliotheks-Assistenten ersetzt.

3.  Um diese Dateien zu verwenden, öffnen Sie das Projekt in Visual J++. Wählen Sie im Menü **Projekt** **Zum Projekt hinzufügen**. Wählen Sie **Dateien**, und fügen Sie alle die. JAVA-Dateien die \\Trustlib-Verzeichnis (standardmäßig unter c:\\Winnt\\Java\\Trustlib\\msado15) zu Ihrem Projekt.

