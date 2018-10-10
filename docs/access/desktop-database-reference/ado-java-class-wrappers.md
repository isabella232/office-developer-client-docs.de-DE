---
title: ADO-Java-Klassenwrapper
TOCTitle: ADO Java Class Wrappers
ms:assetid: de50faf0-80f3-f295-3d9e-3f70f86c3ede
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250126(v=office.15)
ms:contentKeyID: 48548183
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa3a4d1d2a917997b9e7ed5407d4f2ce8d1d0361
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474793"
---
# <a name="ado-java-class-wrappers"></a>ADO-Java-Klassenwrapper


**Betrifft**: Access 2013 | Office 2013

In diesem Code wird in der gleichen Codezeile eine Instanz des Recordset-ADO-Klassenwrappers deklariert und initialisiert. Außerdem werden Variablen für die einzelnen Argumente in der Open-Methode deklariert, insbesondere für LockType und CursorType (da Aufzählungstypen von Java nicht unterstützt werden). Das Recordset-Objekt wird geöffnet und geschlossen. Durch das Festlegen von Rs1 auf NULL wird lediglich geplant, dass diese Variable freigegeben wird, wenn die systematische und periodische Freigabe nicht verwendeter Objekte von Java ausgeführt wird.

```java 
 
public static void main( String args[]) 
{ 
 msado15._Recordset Rs1 = new msado15.Recordset(); 
 Variant Source = new Variant( "SELECT * FROM Authors" ); 
 Variant Connect = new Variant( "DSN=AdoDemo;UID=admin;PWD=;" ); 
 int LockType = msado15.CursorTypeEnum.adOpenForwardOnly; 
 int CursorType = msado15.LockTypeEnum.adLockReadOnly; 
 int Options = -1; 
 
 Rs1.Open( Source, Connect, LockType, CursorType, Options ); 
 Rs1.Close(); 
 Rs1 = null; 
 
 System.out.println( "Success!\n" ); 
} 
```

