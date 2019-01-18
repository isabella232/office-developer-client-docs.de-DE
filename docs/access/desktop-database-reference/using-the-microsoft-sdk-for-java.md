---
title: Verwenden des Microsoft SDK für Java
TOCTitle: Using the Microsoft SDK for Java
ms:assetid: 35a1adb2-06d6-ff45-f151-f1f60ff9bfe2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249116(v=office.15)
ms:contentKeyID: 48544152
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d297d019602cef7b6fbc4f5b0125b87ef642213f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715375"
---
# <a name="using-the-microsoft-sdk-for-java"></a>Verwenden des Microsoft SDK für Java


**Betrifft**: Access 2013, Office 2013

Das Microsoft SDK für Java ist das Entwicklerkit für die Microsoft Internet Explorer-Umgebung. Es werden Tools, Informationen und Beispiele bereitgestellt, um Ihnen beim Entwickeln von Java-Programmen und -Applets zu helfen, die auf JDK 1.1 und Microsoft Win32 Virtual Machine (Microsoft VM) basieren. Das Microsoft SDK für Java ist nicht mit Microsoft Visual J++ verknüpft.

Durch das Hilfsprogramm Jactivex.exe werden Klassen aus einer Typbibliothek generiert, die jedoch nur auf der Befehlszeile aufgerufen werden können. Dieses Feature ist nicht in der Visual J++-Entwicklungsumgebung integriert. Im Gegensatz zu den vom Java-Typbibliotheks-Assistenten generierten Klassen können Sie in die vom SDK erstellten Klassenwrapper springen. Dies ist hilfreich beim Debuggen der Verwendung der ADO-Wrapperklassen durch den Code.

Dieser Mechanismus liest die ADO-Typbibliothek und generiert Klassen, die Sie in der Anwendung instanziieren können. Diese Klassen werden an folgendem Speicherort generiert: \\ \<Windows-Verzeichnis\>\\Java\\Trustlib\\msado15.

Das Erstellen einer ADO-Anwendung in Java mithilfe des Microsoft SDK für Java ist aus der Perspektive des Quellcodes im Grunde identisch mit dem Verwenden des Java-Typbibliotheks-Assistenten. Beispielcode finden Sie unter [ADO-Java-Klassenwrapper](ado-java-class-wrappers.md). Der einzige echte Unterschied besteht in der Generierung der Wrapperklassen, die in den nachstehenden Schritten gezeigt wird.

**So erstellen Sie ein ADO-Projekt mit dem Microsoft SDK für Java**

1.  Führen Sie den folgenden Befehl über eine Eingabeaufforderung aus. Sie müssen den Pfad so festlegen, dass er das Verzeichnis Bin des Microsoft SDK für Java einschließt oder den Befehl von diesem Speicherort ausführen. Normalerweise ist das Microsoft SDK für Java im gleichen Speicherort installiert wie Visual Studio. Dies ist eine Anweisung mit einem einzelnen Befehl.

    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Führen Sie den folgenden Befehl aus, um die generierten Klassen zu kompilieren. Durch den Schalter /g:t wird die Generierung von Debugsymbolen aktiviert, sodass Sie die Java-Symbole verfolgen können. Entfernen Sie sie für Releasebuilds.

    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Um diese Dateien zu verwenden, öffnen Sie das Projekt in Visual J++. Wählen Sie im Menü **Projekt** **Zum Projekt hinzufügen**. Wählen Sie **Dateien**, und fügen Sie alle die. JAVA-Dateien, die in der Trustlib generierte\\msado15-Verzeichnis, um das Projekt.

