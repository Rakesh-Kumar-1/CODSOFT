This is Job Board project which contains php in server side language and mysql as database.
Befor starting you have to create a database in your localhost phpmyadmin.. of name "training"
In training database,you have to create 3 table.

// 1.Table name is "authentication"
CODE:------->>>>
CREATE TABLE `authentication` (
  `id` bigint(250) NOT NULL,
  `firstname` longtext NOT NULL,
  `lastname` longtext NOT NULL,
  `phone` bigint(250) NOT NULL,
  `email` longtext NOT NULL,
  `password` longtext NOT NULL,
  `state` longtext NOT NULL,
  `city` longtext NOT NULL,
  `otp` mediumint(250) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

// 2.Table name is "application"
CODE:------->>>>
CREATE TABLE `application` (
  `id` int(250) NOT NULL,
  `date` date NOT NULL DEFAULT current_timestamp(),
  `email_sender` varchar(250) NOT NULL,
  `authentication_id` int(250) NOT NULL,
  `job_post` longtext NOT NULL,
  `email_reciever` varchar(250) NOT NULL,
  `filename` varchar(250) NOT NULL,
  `filetype` varchar(250) NOT NULL,
  `filesize` int(250) NOT NULL,
  `organization_name` longtext NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

// 3.Table name is "job_form_application"
CODE:------->>>>
CREATE TABLE `job_form_application` (
  `date` date NOT NULL DEFAULT current_timestamp(),
  `id` int(250) NOT NULL,
  `organization_name` longtext NOT NULL,
  `job_post_place` longtext NOT NULL,
  `organization_description` longtext NOT NULL,
  `about_job` longtext NOT NULL,
  `skill_required` longtext NOT NULL,
  `who_can_apply` longtext NOT NULL,
  `salary` longtext NOT NULL,
  `additional_information` longtext NOT NULL,
  `state` longtext NOT NULL,
  `city` longtext NOT NULL,
  `email` longtext NOT NULL,
  `phone` bigint(250) NOT NULL,
  `admin_email` longtext NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
