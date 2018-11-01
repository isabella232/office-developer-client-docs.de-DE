---
title: Handler-Eigenschaft (RDS)
TOCTitle: Handler Property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcb0b7f635e9ad74e6d8733a2f0fbe0153ac4739
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884870"
---
# <a name="handler-property-rds"></a><span data-ttu-id="f6d9a-102">Handler-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="f6d9a-102">Handler Property (RDS)</span></span>


<span data-ttu-id="f6d9a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6d9a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f6d9a-104">Gibt den Name eines serverbasierten Anpassungsprogramms (Handlers) an, das die Funktionalität des [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekts erweitert, sowie alle vom *Handler* verwendeten Parameter.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6d9a-105">Syntax</span></span>

<span data-ttu-id="f6d9a-106">*DataControl*. Handler = *Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f6d9a-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="f6d9a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6d9a-107">Parameters</span></span>

  - <span data-ttu-id="f6d9a-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f6d9a-108">*DataControl*</span></span>

  - <span data-ttu-id="f6d9a-109">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="f6d9a-110">*String*</span><span class="sxs-lookup"><span data-stu-id="f6d9a-110">*String*</span></span>

  - <span data-ttu-id="f6d9a-111">Ein **String** -Wert, der den Namen der Handler und Parameter, alle durch Kommas getrennt (beispielsweise "HandlerName, param1, param2,..., *N*Parameter") enthält.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-111">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6d9a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6d9a-112">Remarks</span></span>

<span data-ttu-id="f6d9a-113">Diese Eigenschaft unterstützt die Anpassung. Bei dieser Funktionalität muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-113">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="f6d9a-p101">Der Name des Handlers und ggf. seiner Parameter werden durch Kommas (",") voneinander getrennt. Ein Semikolon an einer beliebigen Stelle in *String* führt zu unvorhersehbarem Verhalten. Sie können einen eigenen Handler schreiben, er muss jedoch die **IDataFactoryHandler**-Schnittstelle unterstützten.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="f6d9a-p102">Der Name des Standardhandlers lautet **MSDFMAP.Handler**, und sein Standardparameter ist eine Anpassungsdatei mit dem Namen **MSDFMAP.INI**. Rufen Sie mit dieser Eigenschaft alternative Anpassungsdateien auf, die vom Serveradministrator erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f6d9a-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="f6d9a-119">Alternativ zum Festlegen der **Handler** -Eigenschaft ist ein Handler und-Parameter in der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft angegeben. d. h., "\**Handler = \*\*\* HandlerName, param1, param2,...;*".</span><span class="sxs-lookup"><span data-stu-id="f6d9a-119">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

