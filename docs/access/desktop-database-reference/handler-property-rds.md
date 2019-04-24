---
title: Handler-Eigenschaft (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292069"
---
# <a name="handler-property-rds"></a><span data-ttu-id="ec35e-102">Handler-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="ec35e-102">Handler property (RDS)</span></span>

<span data-ttu-id="ec35e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec35e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec35e-104">Gibt den Name eines serverbasierten Anpassungsprogramms (Handlers) an, das die Funktionalität des [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekts erweitert, sowie alle vom *Handler* verwendeten Parameter.</span><span class="sxs-lookup"><span data-stu-id="ec35e-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec35e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec35e-105">Syntax</span></span>

<span data-ttu-id="ec35e-106">*DataControl*. Handler = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="ec35e-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="ec35e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec35e-107">Parameters</span></span>

|<span data-ttu-id="ec35e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec35e-108">Parameter</span></span>|<span data-ttu-id="ec35e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec35e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ec35e-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ec35e-110">*DataControl*</span></span> |<span data-ttu-id="ec35e-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec35e-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="ec35e-112">*String*</span><span class="sxs-lookup"><span data-stu-id="ec35e-112">*String*</span></span> |<span data-ttu-id="ec35e-113">Ein **String** -Wert, der den Namen des Handlers und alle Parameter enthält, die alle durch Kommata getrennt sind (beispielsweise "Handlername, Parm1, Parameter2,..., parm *N*").</span><span class="sxs-lookup"><span data-stu-id="ec35e-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="ec35e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec35e-114">Remarks</span></span>

<span data-ttu-id="ec35e-115">Diese Eigenschaft unterstützt die Anpassung. Bei dieser Funktionalität muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ec35e-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="ec35e-p101">Der Name des Handlers und ggf. seiner Parameter werden durch Kommas (",") voneinander getrennt. Ein Semikolon an einer beliebigen Stelle in *String* führt zu unvorhersehbarem Verhalten. Sie können einen eigenen Handler schreiben, er muss jedoch die **IDataFactoryHandler**-Schnittstelle unterstützten.</span><span class="sxs-lookup"><span data-stu-id="ec35e-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="ec35e-p102">Der Name des Standardhandlers lautet **MSDFMAP.Handler**, und sein Standardparameter ist eine Anpassungsdatei mit dem Namen **MSDFMAP.INI**. Rufen Sie mit dieser Eigenschaft alternative Anpassungsdateien auf, die vom Serveradministrator erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ec35e-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="ec35e-121">Die Alternative zum Festlegen der **Handler** -Eigenschaft besteht darin, einen Handler und Parameter in der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft anzugeben. Das heißt, "\**Handler = \* \* \* Handlername, Parm1, parameter2,...;*".</span><span class="sxs-lookup"><span data-stu-id="ec35e-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

