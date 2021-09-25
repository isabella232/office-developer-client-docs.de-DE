---
title: Gründe für die Verwendung der Outlook-PIA
TOCTitle: Why use the Outlook PIA
ms:assetid: 5cc9085e-7c97-4698-8cb9-e33e427c02e7
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb645534(v=office.15)
ms:contentKeyID: 55119773
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d8b17b49d2ad8f2e197196071c31b66189974ff4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590478"
---
# <a name="why-use-the-outlook-pia"></a>Gründe für die Verwendung der Outlook-PIA

Beginnend mit Outlook 98 stellte Outlook ein Objektmodell für Entwickler bereit, um Outlook-Funktionalitäten in Anwendungen zu integrieren, Outlook zu erweitern oder zu automatisieren. Dieses Objektmodell kann mit der Technologie Component Object Model (COM)-Technologie verwendet werden. In der Vergangenheit entwickelten die Outlook-Anwendungsentwickler COM-Lösungen mithilfe von Visual Basic for Applications (VBA) und Visual Basic. Outlook-Lösungen, die mit VBA entwickelt wurden, wiesen jedoch insbesondere in Unternehmensumgebungen Bereitstellungseinschränkungen auf, und konnten nur schwer nach Bereitstellung aktualisiert werden.

.NET Framework bietet umfassende Klassenbibliotheken und Supporttechnologien, die viele der Einschränkungen von VBA und COM-Add-Ins eliminieren. Eine verwaltete Anwendung benötigt jedoch eine Brücke zwischen .NET und COM-Umgebung, um gegen ein COM-Objektmodell zu programmieren. Eine Interop-Assembly ist ein COM-Wrapper, der als Brücke fungiert. Aus diesem Grund können nun mehr Outlook-Lösungen als verwaltete Anwendung entwickelt werden, die auf einer Interop-Assembly basieren. Weitere Informationen zur vereinfachten Interoperabilität zwischen .NET und COM finden Sie unter [Einführung in die Interoperabilität zwischen COM und .NET](introduction-to-interoperability-between-com-and-net.md).

Eine Interopassembly beschreibt COM-Typen und ermöglicht es verwaltetem Code, mit dem COM-Objektmodell zusammenzuarbeiten. Dabei können unzählige Interopassemblys einen vorhandenen COM-Typ beschreiben. Als Herausgeber der Typbibliothek stellt Outlook eine primäre Interopassembly (PIA) bereit, die die offizielle Beschreibung des COM-basierten Outlook-Objektmodells enthält. Es wird daher empfohlen, die Outlook-PIA zu verwenden, anstatt auf eine Interopassembly einer anderen Quelle zu vertrauen.

## <a name="using-visual-studio-and-office-developer-tools-for-visual-studio"></a>Verwenden von Visual Studio und Office Developer Tools für Visual Studio

Zwar gibt es die Möglichkeit, dass Entwickler verwaltete Outlook-Lösungen außerhalb von Visual Studio entwickeln, aber die Verwendung von Visual Studio erleichtert das Integrieren von Outlook-Funktionalität in verwalteten Code ungemein. Die komfortable und einfache Entwicklung sorgt dafür, dass Add-In-Entwickler von COM zur .NET-Entwicklung migrieren. Entwickler können zur Entwurfszeit die Office Developer Tools in Visual Studio verwenden, um Add-Ins zu erstellen, die sowohl auf das Outlook-Objektmodell als auch auf .NET Framework zugreifen. Zur Laufzeit halten die Office Developer Tools ein Ladeprogramm für die Add-Ins bereit, das beim Start von Outlook die Common Language Runtime (CLR) und die Visual Studio Tools for Office Runtime startet und dann die Add-In-Assembly lädt. Die Assembly kann in Outlook ausgelöste Ereignisse erfassen.

Visual Studio 2012 installiert standardmäßig die Add-In-Vorlagen für Office 2010. Um Office Developer Tools für Visual Studio zum Entwickeln von verwalteten Add-Ins für Outlook 2013 verwenden zu können, müssen Sie die Vorlagen für Office 2013 [herunterladen](https://aka.ms/officedevtoolsforvs2012).

Weitere Informationen zu Office Developer Tools für Visual Studio finden Sie unter [Konfigurieren eines Computers zum Entwickeln von Office-Lösungen](https://docs.microsoft.com/visualstudio/vsto/how-to-configure-a-computer-to-develop-office-solutions?view=vs-2017). Weitere Informationen über die Programmierung von verwalteten Add-Ins für Outlook finden Sie unter [Erste Schritte mit der Programmierung von VSTO-Add-Ins](https://docs.microsoft.com/visualstudio/vsto/getting-started-programming-vsto-add-ins?view=vs-2017).

## <a name="see-also"></a>Siehe auch

- [Installieren der Outlook-PIA und Verweisen auf diese](installing-and-referencing-the-outlook-pia.md)

