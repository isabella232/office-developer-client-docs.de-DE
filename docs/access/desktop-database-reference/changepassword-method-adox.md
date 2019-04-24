---
title: ChangePassword-Methode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df67774b9b38b5fbcc836a2ea0dfc17886d67107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296528"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="304ae-102">ChangePassword-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="304ae-102">ChangePassword method (ADOX)</span></span>

<span data-ttu-id="304ae-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="304ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="304ae-104">Ändert das Kennwort für ein Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="304ae-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="304ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="304ae-105">Syntax</span></span>

<span data-ttu-id="304ae-106">*Benutzer*. ChangePassword*oldPassword*, *Neues Kennwort*</span><span class="sxs-lookup"><span data-stu-id="304ae-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="304ae-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="304ae-107">Parameters</span></span>

|<span data-ttu-id="304ae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="304ae-108">Parameter</span></span>|<span data-ttu-id="304ae-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="304ae-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="304ae-110">*OldPassword*</span><span class="sxs-lookup"><span data-stu-id="304ae-110">*OldPassword*</span></span> |<span data-ttu-id="304ae-111">Ein **String**-Wert, der das aktuelle Kennwort des Benutzers angibt.</span><span class="sxs-lookup"><span data-stu-id="304ae-111">A **String** value that specifies the user's existing password.</span></span> <span data-ttu-id="304ae-112">Wenn der Benutzer aktuell über kein Kennwort verfügt, verwenden Sie für *OldPassword* eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="304ae-112">If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>|
|<span data-ttu-id="304ae-113">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="304ae-113">*NewPassword*</span></span> |<span data-ttu-id="304ae-114">Ein **String**-Wert, der das neue Kennwort angibt.</span><span class="sxs-lookup"><span data-stu-id="304ae-114">A **String** value that specifies the new password.</span></span>|

## <a name="remarks"></a><span data-ttu-id="304ae-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="304ae-115">Remarks</span></span>

<span data-ttu-id="304ae-116">Aus Sicherheitsgründen muss das alte Kennwort zusätzlich zum neuen Kennwort angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="304ae-116">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="304ae-117">Wenn der Anbieter die Verwaltung von Vertrauensnehmereigenschaften nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="304ae-117">An error will occur if the provider does not support the administration of trustee properties.</span></span>

