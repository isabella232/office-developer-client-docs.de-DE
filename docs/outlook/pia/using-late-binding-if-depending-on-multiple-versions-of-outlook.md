---
title: Verwenden von spätem Binden bei mehreren Version von Outlook
TOCTitle: Using late binding if depending on multiple versions of Outlook
ms:assetid: 4e5412a0-d0f8-4819-ba0f-f36ba885f8f6
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610234(v=office.15)
ms:contentKeyID: 55119791
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 866faab04e8fcac1d91b233f801f05c023ac2164
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407072"
---
# <a name="using-late-binding-if-depending-on-multiple-versions-of-outlook"></a>Verwenden von spätem Binden bei mehreren Version von Outlook

Verwaltete Outlook-Add-Ins, die die Outlook Primary Interop Assembly (PIA) verwenden, werden mit den Typinformationen kompiliert, die die von der PIA bereitgestellt werden. Dieses **frühe Binden** von Typinformationen für Methoden und Eigenschaften ermöglicht Typ- und Syntaxprüfungen, um sicherzustellen, dass die richtige Anzahl und die richtigen Typen von Parametern an die Methode oder Eigenschaft übermittelt werden und der erwartete Typ zurückgegeben wird. 

Nachteile frühen Bindens sind eventuelle Versionsinkompatibilitäten bei aufgerufenen Methoden oder Eigenschaften, die abweichende Deklarationen aus früheren Versionen aufweisen. So kann beispielsweise das Hinzufügen neuer Methoden oder Eigenschaften oder das Ändern vorhandener Mitglieder eines Outlook-Objekts das binäre Layout des Objekts verändern und Probleme mit einem verwalteteten Add-In verursachen, das aktuelle Typinformationen zum Automatisieren einer früheren Outlook-Version verwendet. 

In diesen Fällen wartet **spätes Binden** bis zur Laufzeit, um die Eigenschaften und Methoden mit den Objekten zu verbinden. Spätes Binden kann dabei helfen, Versionskonflikte bei Informationen unterschiedlicher Outlook-Versionen zu verhindern, und ist besonders nützlich beim Schreiben von Add-Ins, die von mehreren Outlook-Versionen abhängen.

Das späte Binden umfasst ein Add-In, das die von Outlook implementierte [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nn-oaidl-idispatch)-Schnittstelle aufruft. Um das späte Binden in Visual C\# verwenden zu können, verwenden Sie die [System.Type.InvokeMember](https://docs.microsoft.com/dotnet/api/system.type.invokemember?view=netframework-4.7.2)-Methode. Diese Methode ruft [GetIDsOfNames](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [IDispatch](https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) auf, um die Methoden und Eigenschaften von Outlook zu binden. Mit der IDispatch::GetIDsOfNames-Methode kann Visual C\# ein Objekt darüber abfragen, welche Methoden und Eigenschaften es unterstützt; die IDispatch::Invoke-Methode lässt dann zu, dass Visual C\# diese Methoden und Eigenschaften aufruft. 

<!-- PAGES 404 
For more information about using late binding in C\#, see [KB 302902: Binding for Office Automation Servers with Visual C\# .NET](https://go.microsoft.com/fwlink/?linkid=88971). For more information about using late binding in Visual Basic, see [KB 304661: How to Use Visual Basic .NET for Binding for Office Automation Servers](https://go.microsoft.com/fwlink/?linkid=88972).

Note that late binding requires obtaining a DispID for every method or property, so late binding generally does not perform as well as early binding. For more information about how early binding compares with late binding, see [KB 245115: Using Early Binding and Late Binding in Automation](https://go.microsoft.com/fwlink/?linkid=88973). -->

## <a name="see-also"></a>Siehe auch

- [Einführung in die Interoperabilität zwischen COM und .NET](introduction-to-interoperability-between-com-and-net.md)

