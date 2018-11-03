---
title: DBEngine.IniPath-Eigenschaft (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fd744f10d212d8ff0f7c78ca72781869ccdcd57e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928761"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="2ad58-102">DBEngine.IniPath-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ad58-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="2ad58-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ad58-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ad58-104">Legt Informationen über den Windows-Registrierungsschlüssel fest, der Werte für die Microsoft Access-Datenbank-Engine enthält, oder gibt die Informationen zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="2ad58-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ad58-105">Syntax</span></span>

<span data-ttu-id="2ad58-106">*Ausdruck* . IniPath</span><span class="sxs-lookup"><span data-stu-id="2ad58-106">*expression* .IniPath</span></span>

<span data-ttu-id="2ad58-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ad58-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ad58-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ad58-108">Remarks</span></span>

<span data-ttu-id="2ad58-p101">Sie können die Microsoft Access-Datenbank-Engine mit der Windows-Registrierung konfigurieren. Mit der Registrierung können Sie Optionen festlegen, wie etwa installierbare ISAM-DLL-Dateien.</span><span class="sxs-lookup"><span data-stu-id="2ad58-p101">You can configure the Microsoft Access databse engine with the Windows Registry. You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="2ad58-p102">Damit diese Option wirksam wird, müssen Sie die **IniPath**-Eigenschaft festlegen, bevor Ihre Anwendung einen anderen DAO-Code aufruft. Die Wirkung dieser Einstellung ist auf die Anwendung begrenzt. Sie kann nur geändert werden, wenn Sie die Anwendung neu starten.</span><span class="sxs-lookup"><span data-stu-id="2ad58-p102">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code. The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="2ad58-p103">Die Registrierung dient auch zur Bereitstellung von Initialisierungsparametern für einige installierbare ISAM-Datenbanktreiber. Beispiel: Zur Verwendung von Paradox Version 4.0 legen Sie für die **IniPath**-Eigenschaft den Teil der Registrierung fest, der die betreffenden Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="2ad58-p103">You also use the Registry to provide initialization parameters for some installable ISAM database drivers. For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="2ad58-115">Diese Eigenschaft erkennt entweder HKEY\_lokale\_Computer oder HKEY\_lokale\_Benutzer.</span><span class="sxs-lookup"><span data-stu-id="2ad58-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="2ad58-116">Wenn kein Stammschlüssel bereitgestellt wird, wird der Standardwert ist HKEY\_lokale\_Computer.</span><span class="sxs-lookup"><span data-stu-id="2ad58-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

