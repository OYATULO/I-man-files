# Добавлено новый таблица тип банка
CREATE TABLE `i-man`.`typebank` (
  `Id` INT NOT NULL AUTO_INCREMENT,
  `Name` VARCHAR(45) NULL,
  PRIMARY KEY (`Id`))
ENGINE = InnoDB
DEFAULT CHARACTER SET = utf8;
# Обновит таб Sales 
ALTER TABLE `i-man`.`sales` 
ADD COLUMN `Bank` INT(11) NULL DEFAULT NULL AFTER `clientdata`;
# Обновит таблица Users
ALTER TABLE `i-man`.`users` 
ADD COLUMN `Macaddress` VARCHAR(45) NULL AFTER `RoleId`;
# Добавит таблица Отчет по ревизия 
   CREATE TABLE `i-man`.`mdaftereditrevision` (
  `ID` INT NOT NULL AUTO_INCREMENT,
  `Sklad` VARCHAR(45) NULL,
  `Namegoods` VARCHAR(255) NULL,
  `D_srok` DATETIME NULL,
  `Price` DECIMAL(18,2) NULL,
  `Summa` DECIMAL(18,2) NULL,
  `Barcode` VARCHAR(255) NULL,
  `UnitAmount` INT NULL DEFAULT NULL,
  `AmountContainer` INT NULL,
  `AmountUnit` INT NULL,
  `I_AmountContainer` INT NULL,
  `I_AmountUnit` INT NULL,
  `N_AmountContainer` INT NULL,
  `N_AmountUnit` INT NULL,
  `Polka` VARCHAR(128) NULL,
  `Checked` TINYINT NULL,
  `User` VARCHAR(45) NULL AFTER,
  `Date_inserted` DATETIME NULL
  PRIMARY KEY (`ID`))
ENGINE = InnoDB
DEFAULT CHARACTER SET = utf8;

 # I-man-files
