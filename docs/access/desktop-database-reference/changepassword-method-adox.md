---
title: ChangePassword-Methode (ADOX)
TOCTitle: ChangePassword method (ADOX)
ms:assetid: 999826a5-3e6b-b6da-b8f6-d61b9a50ceca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249690(v=office.15)
ms:contentKeyID: 48546519
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7eef5fc93f9cce68e6342b62c1ab07ee6f65587f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946020"
---
# <a name="changepassword-method-adox"></a><span data-ttu-id="b0e93-102">ChangePassword-Methode (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b0e93-102">ChangePassword method (ADOX)</span></span>


<span data-ttu-id="b0e93-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0e93-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="b0e93-104">Ändert das Kennwort für ein Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="b0e93-104">Changes the password for a user account.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0e93-105">Syntax</span></span>

<span data-ttu-id="b0e93-106">*Benutzer*. ChangePassword*AltesKennwort*, *NewPassword*</span><span class="sxs-lookup"><span data-stu-id="b0e93-106">*User*.ChangePassword*OldPassword*, *NewPassword*</span></span>

## <a name="parameters"></a><span data-ttu-id="b0e93-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b0e93-107">Parameters</span></span>

- <span data-ttu-id="b0e93-108">*AltesKennwort*</span><span class="sxs-lookup"><span data-stu-id="b0e93-108">*OldPassword*</span></span>

  - <span data-ttu-id="b0e93-p101">Ein **String**-Wert, der das aktuelle Kennwort des Benutzers angibt. Wenn der Benutzer aktuell über kein Kennwort verfügt, verwenden Sie für *OldPassword* eine leere Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="b0e93-p101">A **String** value that specifies the user's existing password. If the user doesn't currently have a password, use an empty string ("") for *OldPassword*.</span></span>

- <span data-ttu-id="b0e93-111">*NewPassword*</span><span class="sxs-lookup"><span data-stu-id="b0e93-111">*NewPassword*</span></span>

  - <span data-ttu-id="b0e93-112">Ein **String** -Wert, der das neue Kennwort angibt.</span><span class="sxs-lookup"><span data-stu-id="b0e93-112">A **String** value that specifies the new password.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e93-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0e93-113">Remarks</span></span>

<span data-ttu-id="b0e93-114">Aus Sicherheitsgründen muss das alte Kennwort zusätzlich zum neuen Kennwort angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b0e93-114">For security reasons, the old password must be specified in addition to the new password.</span></span>

<span data-ttu-id="b0e93-115">Wenn der Anbieter die Verwaltung von Vertrauensnehmereigenschaften nicht unterstützt, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b0e93-115">An error will occur if the provider does not support the administration of trustee properties.</span></span>

