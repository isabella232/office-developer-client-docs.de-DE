---
title: Anpassen der Windows-Registrierungseinstellungen für Microsoft Access-Datenbankmodul
TOCTitle: Customizing Windows Registry Settings for the Microsoft Access Database Engine
ms:assetid: ca7e958a-ea26-d67d-45b9-10aeb1eac96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834346(v=office.15)
ms:contentKeyID: 48547690
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032168
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a44226e8ea90a8be96de35cdc923349eded17cb4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886998"
---
# <a name="customizing-windows-registry-settings-for-the-microsoft-access-database-engine"></a><span data-ttu-id="59f3b-102">Anpassen der Einstellungen in der Windows-Registrierung für das Microsoft Access-Datenbankmodul</span><span class="sxs-lookup"><span data-stu-id="59f3b-102">Customizing Windows Registry Settings for the Microsoft Access Database Engine</span></span>


<span data-ttu-id="59f3b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59f3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59f3b-p101">Wenn Ihre Anwendung mit den Standardfunktionen des Microsoft Access-Datenbankmoduls nicht ordnungsgemäß ausgeführt wird, müssen Sie möglicherweise die Einstellungen in der Microsoft® Windows®-Registrierung an Ihre Bedürfnisse anpassen. Mithilfe der Windows-Registrierung können Sie auch die Arbeitsweise der installierbaren ISAM- nd ODBC-Treiber optimieren.</span><span class="sxs-lookup"><span data-stu-id="59f3b-p101">If your application cannot work correctly with the default functionality of the Microsoft Access database engine, you may have to change the settings in the Microsoft® Windows® Registry to suit your needs. The Windows Registry can also be used to tune the operation of the installable ISAM and ODBC driver.</span></span>

<span data-ttu-id="59f3b-106">Es gibt vier verschiedene Möglichkeiten, die Einstellungen in der Windows-Registrierung anzupassen:</span><span class="sxs-lookup"><span data-stu-id="59f3b-106">You can customize the settings in the Windows Registry in four different ways:</span></span>

<span data-ttu-id="59f3b-107">[Verwenden von "Regedit.exe" zum Überschreiben der Standardeinstellungen](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="59f3b-107">[Using Regedit.exe to Overwrite the Default Settings](https://msdn.microsoft.com/library/ff193205\(v=office.15\))</span></span>

<span data-ttu-id="59f3b-108">[Erstellen eines Teils im Registrierungsbaum Ihrer Anwendung zur Verwaltung der Einstellungen](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="59f3b-108">[Creating a Portion in Your Application's Registry Tree to Manage the Settings](https://msdn.microsoft.com/library/ff836342\(v=office.15\))</span></span>

<span data-ttu-id="59f3b-109">[Verwenden der SetOption-Methode von DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="59f3b-109">[Using the SetOption Method from DAO](https://msdn.microsoft.com/library/ff194471\(v=office.15\))</span></span>

<span data-ttu-id="59f3b-110">[Verwenden der Verbindungseigenschaften im Microsoft OLE DB Provider für Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="59f3b-110">[Using the Connection Properties in the Microsoft OLE DB Provider for Access](https://msdn.microsoft.com/library/ff196356\(v=office.15\))</span></span>

