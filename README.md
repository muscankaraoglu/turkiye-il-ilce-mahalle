# 2021 - Türkiye İller, İlçeler ve Mahalleler MSSQL Insert Sorgusu (Turkey City, District, Neighborhood SQL Insert Query)

    City
      |-District
        |- Neighborhood

Şeklinde ilişkilendirilmiş tablolar için uygundur. (Suitable for tables relationed like above).


## Cities

    CREATE TABLE [dbo].[Cities](
		[Id] [int] IDENTITY(1,1) NOT NULL,
		[Name] [nvarchar](max) NULL)
## Districts

    CREATE TABLE [dbo].[Districts](
		[Id] [int] IDENTITY(1,1) NOT NULL,
		[Name] [nvarchar](max) NULL,
		[CityId] [int] NOT NULL)
## Neighborhoods

     CREATE TABLE [dbo].[Neighborhoods](
    	[Id] [int] IDENTITY(1,1) NOT NULL,
    	[Name] [nvarchar](max) NULL,
    	[DistrictId] [int] NOT NULL)
